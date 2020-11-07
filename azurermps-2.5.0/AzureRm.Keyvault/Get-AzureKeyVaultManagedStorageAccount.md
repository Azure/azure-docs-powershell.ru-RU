---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
ms.openlocfilehash: 51e7b941e5dbb4d07b48444196f6e3d3aa830452
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914121"
---
# <span data-ttu-id="51982-101">Get-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="51982-101">Get-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="51982-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="51982-102">SYNOPSIS</span></span>
<span data-ttu-id="51982-103">Получение управляемых учетных записей хранилища Azure для хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="51982-103">Gets Key Vault managed Azure Storage Accounts.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51982-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="51982-104">SYNTAX</span></span>

### <span data-ttu-id="51982-105">ByVaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="51982-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="51982-106">ByAccountName</span><span class="sxs-lookup"><span data-stu-id="51982-106">ByAccountName</span></span>
```
Get-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51982-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="51982-107">DESCRIPTION</span></span>
<span data-ttu-id="51982-108">Возвращает управляемую учетную запись хранилища Azure с основным хранилищем, если указано имя учетной записи, а ключи учетной записи управляются указанным хранилищем.</span><span class="sxs-lookup"><span data-stu-id="51982-108">Gets a Key Vault managed Azure Storage Account if the name of the account is specified and the account keys are managed by the specified vault.</span></span> <span data-ttu-id="51982-109">Если имя учетной записи не указано, перечисляются все учетные записи, для которых управление ключами задается указанным хранилищем.</span><span class="sxs-lookup"><span data-stu-id="51982-109">If the account name is not specified, then all the accounts whose keys are managed by specified vault are listed.</span></span>

## <span data-ttu-id="51982-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="51982-110">EXAMPLES</span></span>

### <span data-ttu-id="51982-111">Пример 1: список всех учетных записей хранения с управляемым хранилищем</span><span class="sxs-lookup"><span data-stu-id="51982-111">Example 1: List all Key Vault managed Storage Accounts</span></span>
```
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName 'myvault'
```

<span data-ttu-id="51982-112">Выводит все учетные записи, для которых управление ключами является хранилищем "myvault".</span><span class="sxs-lookup"><span data-stu-id="51982-112">Lists all the accounts whose keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="51982-113">Пример 2: получение учетной записи хранилища с управляемым хранилищем ключей</span><span class="sxs-lookup"><span data-stu-id="51982-113">Example 2: Get a Key Vault managed Storage Account</span></span>
```
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -Name 'mystorageaccount'
```

<span data-ttu-id="51982-114">Получение сведений об учетной записи хранения ключа управляемого хранилища для "mystorageaccount", если ее ключи управляются хранилищем "myvault"</span><span class="sxs-lookup"><span data-stu-id="51982-114">Gets the details of Key Vault managed Storage Account of 'mystorageaccount' if its keys are managed by vault 'myvault'</span></span>

## <span data-ttu-id="51982-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="51982-115">PARAMETERS</span></span>

### <span data-ttu-id="51982-116">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="51982-116">-AccountName</span></span>
<span data-ttu-id="51982-117">Имя учетной записи хранилища с управляемым хранилищем.</span><span class="sxs-lookup"><span data-stu-id="51982-117">Key Vault managed storage account name.</span></span> <span data-ttu-id="51982-118">Командлет создает полное доменное имя управляемой учетной записи хранения из имени хранилища, выбранной в данный момент среды и управляемого имени учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="51982-118">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: String
Parameter Sets: ByAccountName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51982-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51982-119">-DefaultProfile</span></span>
<span data-ttu-id="51982-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="51982-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="51982-121">-VaultName</span><span class="sxs-lookup"><span data-stu-id="51982-121">-VaultName</span></span>
<span data-ttu-id="51982-122">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="51982-122">Vault name.</span></span>
<span data-ttu-id="51982-123">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="51982-123">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="51982-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51982-124">CommonParameters</span></span>
<span data-ttu-id="51982-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="51982-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51982-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51982-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51982-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="51982-127">INPUTS</span></span>

### <span data-ttu-id="51982-128">System. String</span><span class="sxs-lookup"><span data-stu-id="51982-128">System.String</span></span>

## <span data-ttu-id="51982-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="51982-129">OUTPUTS</span></span>

### <span data-ttu-id="51982-130">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. KeyVault. Models. ManagedStorageAccount, Microsoft. Azure. Commands. KeyVault, Version = 2.5.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="51982-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount, Microsoft.Azure.Commands.KeyVault, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="51982-131">Microsoft. Azure. Commands. KeyVault. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="51982-131">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="51982-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="51982-132">NOTES</span></span>

## <span data-ttu-id="51982-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="51982-133">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

