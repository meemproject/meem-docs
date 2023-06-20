# Working with Community Agreements

Meem communities all have their own unique Community Agreement smart contract. Your extension can access all information in the community agreement.

We've created convenience properties to access your community Agreement and Extension data:

```typescript
const { agreement, isLoadingAgreement } = useAgreement()
const agreementExtension = extensionFromSlug('example', agreement)
```

### **Agreements**

Agreements are the smart contract that is the foundation of your community.

```typescript
export interface Agreement {
	address?: string // The agreement contract address
	adminAddresses?: string[] // Contract admin addresses
	admins?: AgreementMember[] // Contract admins
	agreementOwner?: AgreementMember
	description?: string
	extensions?: AgreementExtensions[] // Extensions enabled for this community
	gnosisSafeAddress?: string | null
	id?: string
	image?: string
	isAgreementControlledByMeemApi?: boolean
	isCurrentUserAgreementAdmin?: boolean
	isCurrentUserAgreementMember?: boolean
	isCurrentUserAgreementOwner?: boolean
	isLaunched?: boolean
	isValid?: boolean
	memberCount?: number
	memberRolesMap?: Map<string, AgreementMember[]>
	members?: AgreementMember[] // Members of the Community Agreement
	membershipSettings?: MembershipSettings
	membershipToken?: string
	name?: string
	rawAgreement?: Agreements
	roles?: AgreementRole[] // The Agreement roles
	slotsLeft?: number
	slug?: string
}
```



### Agreement Roles

Within the community Agreement you can access any Agreement Roles that belong to the community via the `roles` property. These are their own unique smart contracts that are owned by the community.

```typescript
export interface AgreementRole {
	id: string
	isAdminRole?: boolean // If this is the admin role of the Community Agreement.
	isTransferrable?: boolean
	name: string
	rolesExtensionData?: any
	tokenAddress?: string // The role contract address
}
```



### **Agreement Extensions**

Any enabled community extensions data is accessible via the `extensions` property of the Agreement.&#x20;

```typescript
type AgreementExtensions = {
  /** Agreement extension links (DEPRECATED) */
  AgreementExtensionLinks: Array<AgreementExtensionLinks>;
  /** Agreement extension widgets */
  AgreementExtensionWidgets: Array<AgreementExtensionWidgets>;
  /** The parent extension data */
  Extension?: Maybe<Extensions>;
  /** The parent extension id  */
  ExtensionId?: Maybe<Scalars['uuid']>;
  createdAt: Scalars['timestamptz'];
  /** This community extension's id */
  id: Scalars['uuid'];
  /** Whether the extension configuration has been completed */
  isInitialized?: Maybe<Scalars['Boolean']>;
  /** Extension configuration data for this community extension instance */
  metadata?: Maybe<Scalars['jsonb']>;
  updatedAt: Scalars['timestamptz'];
};
```

