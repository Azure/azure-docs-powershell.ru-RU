---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurekeyvaultmanagedstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccountKey.md
ms.openlocfilehash: 317a7f72e68f442608a0b163afd99af6eaac28c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561740"
---
# <span data-ttu-id="46992-101">Update-AzureKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="46992-101">Update-AzureKeyVaultManagedStorageAccountKey</span></span>

## <span data-ttu-id="46992-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="46992-102">SYNOPSIS</span></span>
<span data-ttu-id="46992-103">Повторное создание указанного ключа учетной записи хранения для хранилища ключей из управляемого хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="46992-103">Regenerates the specified key of Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46992-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="46992-104">SYNTAX</span></span>

```
Update-AzureKeyVaultManagedStorageAccountKey [-VaultName] <String> [-AccountName] <String> [-KeyName] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46992-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="46992-105">DESCRIPTION</span></span>
<span data-ttu-id="46992-106">Повторное создание указанного ключа учетной записи хранилища для управляемого хранилища Azure и задание ключа в качестве активного ключа.</span><span class="sxs-lookup"><span data-stu-id="46992-106">Regenerates the specified key of Key Vault managed Azure Storage Account and sets the key as the active key.</span></span> <span data-ttu-id="46992-107">Прокси-сервер хранилища ключей. вызов в диспетчере ресурсов Azure для повторного создания ключа.</span><span class="sxs-lookup"><span data-stu-id="46992-107">Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span></span> <span data-ttu-id="46992-108">Вызывающий объект должен posses разрешения на повторное создание ключей в указанной учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="46992-108">The caller must posses permissions to regenerate keys on given Azure Storage Account.</span></span>

## <span data-ttu-id="46992-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="46992-109">EXAMPLES</span></span>

### <span data-ttu-id="46992-110">Пример 1: повторное создание ключа</span><span class="sxs-lookup"><span data-stu-id="46992-110">Example 1: Regenerate a key</span></span>
```
PS C:\> Update-AzureKeyVaultManagedStorageAccountKey -VaultName 'myvault' -AccountName 'mystorageaccount' -KeyName 'key1'
```

<span data-ttu-id="46992-111">Повторное создание "key1" учетной записи "mystorageaccount" и установка "key1" в качестве активной учетной записи хранения для хранилища ключей в службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="46992-111">Regenerates 'key1' of account 'mystorageaccount' and sets 'key1' as the active of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="46992-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="46992-112">PARAMETERS</span></span>

### <span data-ttu-id="46992-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="46992-113">-AccountName</span></span>
<span data-ttu-id="46992-114">Имя учетной записи хранилища с управляемым хранилищем.</span><span class="sxs-lookup"><span data-stu-id="46992-114">Key Vault managed storage account name.</span></span> <span data-ttu-id="46992-115">Командлет создает полное доменное имя управляемой учетной записи хранения из имени хранилища, выбранной в данный момент среды и управляемого имени учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="46992-115">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46992-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46992-116">-DefaultProfile</span></span>
<span data-ttu-id="46992-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="46992-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46992-118">-Force</span><span class="sxs-lookup"><span data-stu-id="46992-118">-Force</span></span>
<span data-ttu-id="46992-119">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="46992-119">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46992-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="46992-120">-KeyName</span></span>
<span data-ttu-id="46992-121">Имя ключа учетной записи хранения, которое нужно повторно создать и сделать активным.</span><span class="sxs-lookup"><span data-stu-id="46992-121">Name of storage account key to regenerate and make active.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46992-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="46992-122">-PassThru</span></span>
<span data-ttu-id="46992-123">По умолчанию командлет не возвращает объект.</span><span class="sxs-lookup"><span data-stu-id="46992-123">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="46992-124">Если этот параметр указан, командлет возвращает управляемую учетную запись хранения, которая была удалена.</span><span class="sxs-lookup"><span data-stu-id="46992-124">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46992-125">-VaultName</span><span class="sxs-lookup"><span data-stu-id="46992-125">-VaultName</span></span>
<span data-ttu-id="46992-126">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="46992-126">Vault name.</span></span>
<span data-ttu-id="46992-127">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="46992-127">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="46992-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="46992-128">-Confirm</span></span>
<span data-ttu-id="46992-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="46992-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46992-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46992-130">-WhatIf</span></span>
<span data-ttu-id="46992-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="46992-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46992-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="46992-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46992-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46992-133">CommonParameters</span></span>
<span data-ttu-id="46992-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="46992-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46992-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46992-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46992-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="46992-136">INPUTS</span></span>

### <span data-ttu-id="46992-137">System. String</span><span class="sxs-lookup"><span data-stu-id="46992-137">System.String</span></span>

## <span data-ttu-id="46992-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="46992-138">OUTPUTS</span></span>

### <span data-ttu-id="46992-139">Microsoft. Azure. Commands. KeyVault. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46992-139">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="46992-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="46992-140">NOTES</span></span>

## <span data-ttu-id="46992-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="46992-141">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

