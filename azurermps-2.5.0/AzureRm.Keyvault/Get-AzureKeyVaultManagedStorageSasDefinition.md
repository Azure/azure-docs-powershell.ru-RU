---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultmanagedstoragesasdefinition
schema: 2.0.0
ms.openlocfilehash: 6a1994979cc6521cee083b07f336a76a54dd7cb7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914117"
---
# <span data-ttu-id="5ff2e-101">Get-AzureKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="5ff2e-101">Get-AzureKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="5ff2e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5ff2e-102">SYNOPSIS</span></span>
<span data-ttu-id="5ff2e-103">Получение определений SAS хранилища, управляемого основным хранилищем.</span><span class="sxs-lookup"><span data-stu-id="5ff2e-103">Gets Key Vault managed Storage SAS Definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ff2e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5ff2e-104">SYNTAX</span></span>

### <span data-ttu-id="5ff2e-105">ByAccountName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5ff2e-105">ByAccountName (Default)</span></span>
```
Get-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ff2e-106">ByDefinitionName</span><span class="sxs-lookup"><span data-stu-id="5ff2e-106">ByDefinitionName</span></span>
```
Get-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ff2e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ff2e-107">DESCRIPTION</span></span>
<span data-ttu-id="5ff2e-108">Возвращает определение SAS хранилища управляемых хранилищ, если указано имя определения.</span><span class="sxs-lookup"><span data-stu-id="5ff2e-108">Gets a Key Vault managed Storage SAS Definition if the name of the definition is specified.</span></span> <span data-ttu-id="5ff2e-109">Если имя определения не задано, в списке будут перечислены все определения SAS, связанные с указанной учетной записью в хранилище ключей, управляемой в хранилище.</span><span class="sxs-lookup"><span data-stu-id="5ff2e-109">If the definition name is not specified, then all the SAS definitions associated with the specified Key Vault managed Storage Account in the vault are listed.</span></span>

## <span data-ttu-id="5ff2e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5ff2e-110">EXAMPLES</span></span>

### <span data-ttu-id="5ff2e-111">Пример 1: список всех определений SAS хранилища, управляемых основным хранилищем</span><span class="sxs-lookup"><span data-stu-id="5ff2e-111">Example 1: List all Key Vault managed Storage SAS Definitions</span></span>
```
PS C:\> Get-AzureKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount'
```

<span data-ttu-id="5ff2e-112">В этой статье перечислены все определения SAS, связанные с учетной записью хранилища с управляемым хранилищем "mystorageaccount", управляемой хранилищем "myvault"</span><span class="sxs-lookup"><span data-stu-id="5ff2e-112">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'</span></span>

### <span data-ttu-id="5ff2e-113">Пример 2: получение учетной записи хранилища с управляемым хранилищем ключей</span><span class="sxs-lookup"><span data-stu-id="5ff2e-113">Example 2: Get a Key Vault managed Storage Account</span></span>
```
PS C:\> Get-AzureKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasDef'
```

<span data-ttu-id="5ff2e-114">Получает подробные сведения об определении SAS "mysasDef", связанном с учетной записью хранилища с управляемым хранилищем "mystorageaccount", управляемой хранилищем "myvault".</span><span class="sxs-lookup"><span data-stu-id="5ff2e-114">Gets the details of SAS Definition 'mysasDef' associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'.</span></span>

## <span data-ttu-id="5ff2e-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5ff2e-115">PARAMETERS</span></span>

### <span data-ttu-id="5ff2e-116">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="5ff2e-116">-AccountName</span></span>
<span data-ttu-id="5ff2e-117">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="5ff2e-117">Vault name.</span></span>
<span data-ttu-id="5ff2e-118">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="5ff2e-118">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ff2e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ff2e-119">-DefaultProfile</span></span>
<span data-ttu-id="5ff2e-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5ff2e-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ff2e-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5ff2e-121">-Name</span></span>
<span data-ttu-id="5ff2e-122">Имя определения SAS хранилища.</span><span class="sxs-lookup"><span data-stu-id="5ff2e-122">Storage sas definition name.</span></span>
<span data-ttu-id="5ff2e-123">Командлет создает полное доменное имя определения SAS хранилища из имени хранилища, выбранной среды, имени учетной записи хранения и имени определения SAS.</span><span class="sxs-lookup"><span data-stu-id="5ff2e-123">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: String
Parameter Sets: ByDefinitionName
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ff2e-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="5ff2e-124">-VaultName</span></span>
<span data-ttu-id="5ff2e-125">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="5ff2e-125">Vault name.</span></span>
<span data-ttu-id="5ff2e-126">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="5ff2e-126">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ff2e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ff2e-127">CommonParameters</span></span>
<span data-ttu-id="5ff2e-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5ff2e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ff2e-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ff2e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ff2e-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5ff2e-130">INPUTS</span></span>

### <span data-ttu-id="5ff2e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="5ff2e-131">System.String</span></span>

## <span data-ttu-id="5ff2e-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ff2e-132">OUTPUTS</span></span>

### <span data-ttu-id="5ff2e-133">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. KeyVault. Models. ManagedStorageSasDefinitionListItem, Microsoft. Azure. Commands. KeyVault, Version = 2.5.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="5ff2e-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinitionListItem, Microsoft.Azure.Commands.KeyVault, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="5ff2e-134">Microsoft. Azure. Commands. KeyVault. Models. ManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="5ff2e-134">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinition</span></span>

## <span data-ttu-id="5ff2e-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="5ff2e-135">NOTES</span></span>

## <span data-ttu-id="5ff2e-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5ff2e-136">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

