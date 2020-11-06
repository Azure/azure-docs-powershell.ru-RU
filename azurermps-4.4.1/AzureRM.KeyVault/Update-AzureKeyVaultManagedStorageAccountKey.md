---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccountKey.md
ms.openlocfilehash: 94e1b297879e31ff42f9c12c0e4ad4a601e5e163
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567608"
---
# <span data-ttu-id="4e0ee-101">Update-AzureKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="4e0ee-101">Update-AzureKeyVaultManagedStorageAccountKey</span></span>

## <span data-ttu-id="4e0ee-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4e0ee-102">SYNOPSIS</span></span>
<span data-ttu-id="4e0ee-103">Повторное создание указанного ключа учетной записи хранения для хранилища ключей из управляемого хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4e0ee-103">Regenerates the specified key of Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e0ee-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4e0ee-104">SYNTAX</span></span>

```
Update-AzureKeyVaultManagedStorageAccountKey [-VaultName] <String> [-AccountName] <String> [-KeyName] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e0ee-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e0ee-105">DESCRIPTION</span></span>
<span data-ttu-id="4e0ee-106">Повторное создание указанного ключа учетной записи хранилища для управляемого хранилища Azure и задание ключа в качестве активного ключа.</span><span class="sxs-lookup"><span data-stu-id="4e0ee-106">Regenerates the specified key of Key Vault managed Azure Storage Account and sets the key as the active key.</span></span> <span data-ttu-id="4e0ee-107">Прокси-сервер хранилища ключей. вызов в диспетчере ресурсов Azure для повторного создания ключа.</span><span class="sxs-lookup"><span data-stu-id="4e0ee-107">Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span></span> <span data-ttu-id="4e0ee-108">Вызывающий объект должен posses разрешения на повторное создание ключей в указанной учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="4e0ee-108">The caller must posses permissions to regenerate keys on given Azure Storage Account.</span></span>

## <span data-ttu-id="4e0ee-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4e0ee-109">EXAMPLES</span></span>

### <span data-ttu-id="4e0ee-110">Пример 1: повторное создание ключа</span><span class="sxs-lookup"><span data-stu-id="4e0ee-110">Example 1: Regenerate a key</span></span>
```
PS C:\> Update-AzureKeyVaultManagedStorageAccountKey -VaultName 'myvault' -AccountName 'mystorageaccount' -KeyName 'key1'
```

<span data-ttu-id="4e0ee-111">Повторное создание "key1" учетной записи "mystorageaccount" и установка "key1" в качестве активной учетной записи хранения для хранилища ключей в службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4e0ee-111">Regenerates 'key1' of account 'mystorageaccount' and sets 'key1' as the active of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="4e0ee-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4e0ee-112">PARAMETERS</span></span>

### <span data-ttu-id="4e0ee-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="4e0ee-113">-AccountName</span></span>
<span data-ttu-id="4e0ee-114">Имя учетной записи хранилища с управляемым хранилищем.</span><span class="sxs-lookup"><span data-stu-id="4e0ee-114">Key Vault managed storage account name.</span></span> <span data-ttu-id="4e0ee-115">Командлет создает полное доменное имя управляемой учетной записи хранения из имени хранилища, выбранной в данный момент среды и управляемого имени учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="4e0ee-115">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e0ee-116">-Force</span><span class="sxs-lookup"><span data-stu-id="4e0ee-116">-Force</span></span>
<span data-ttu-id="4e0ee-117">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="4e0ee-117">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e0ee-118">-KeyName</span><span class="sxs-lookup"><span data-stu-id="4e0ee-118">-KeyName</span></span>
<span data-ttu-id="4e0ee-119">Имя ключа учетной записи хранения, которое нужно повторно создать и сделать активным.</span><span class="sxs-lookup"><span data-stu-id="4e0ee-119">Name of storage account key to regenerate and make active.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e0ee-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e0ee-120">-PassThru</span></span>
<span data-ttu-id="4e0ee-121">По умолчанию командлет не возвращает объект.</span><span class="sxs-lookup"><span data-stu-id="4e0ee-121">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="4e0ee-122">Если этот параметр указан, командлет возвращает управляемую учетную запись хранения, которая была удалена.</span><span class="sxs-lookup"><span data-stu-id="4e0ee-122">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e0ee-123">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4e0ee-123">-VaultName</span></span>
<span data-ttu-id="4e0ee-124">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="4e0ee-124">Vault name.</span></span>
<span data-ttu-id="4e0ee-125">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="4e0ee-125">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e0ee-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e0ee-126">-Confirm</span></span>
<span data-ttu-id="4e0ee-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4e0ee-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e0ee-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e0ee-128">-WhatIf</span></span>
<span data-ttu-id="4e0ee-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4e0ee-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e0ee-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4e0ee-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e0ee-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e0ee-131">-DefaultProfile</span></span>
<span data-ttu-id="4e0ee-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e0ee-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e0ee-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e0ee-133">CommonParameters</span></span>
<span data-ttu-id="4e0ee-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4e0ee-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e0ee-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e0ee-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e0ee-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4e0ee-136">INPUTS</span></span>

### <span data-ttu-id="4e0ee-137">System. String</span><span class="sxs-lookup"><span data-stu-id="4e0ee-137">System.String</span></span>

## <span data-ttu-id="4e0ee-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e0ee-138">OUTPUTS</span></span>

### <span data-ttu-id="4e0ee-139">Microsoft. Azure. Commands. KeyVault. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4e0ee-139">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="4e0ee-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="4e0ee-140">NOTES</span></span>

## <span data-ttu-id="4e0ee-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e0ee-141">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

