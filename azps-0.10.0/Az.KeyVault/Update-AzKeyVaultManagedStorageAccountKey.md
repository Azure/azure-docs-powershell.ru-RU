---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/update-AzKeyvaultmanagedstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
ms.openlocfilehash: d73e9b02940f98db6734f851219399a2ba6c74a2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911139"
---
# <span data-ttu-id="ca42c-101">Update-AzKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="ca42c-101">Update-AzKeyVaultManagedStorageAccountKey</span></span>

## <span data-ttu-id="ca42c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ca42c-102">SYNOPSIS</span></span>
<span data-ttu-id="ca42c-103">Повторное создание указанного ключа учетной записи хранения для хранилища ключей из управляемого хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="ca42c-103">Regenerates the specified key of Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="ca42c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ca42c-104">SYNTAX</span></span>

```
Update-AzKeyVaultManagedStorageAccountKey [-VaultName] <String> [-AccountName] <String> [-KeyName] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca42c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca42c-105">DESCRIPTION</span></span>
<span data-ttu-id="ca42c-106">Повторное создание указанного ключа учетной записи хранилища для управляемого хранилища Azure и задание ключа в качестве активного ключа.</span><span class="sxs-lookup"><span data-stu-id="ca42c-106">Regenerates the specified key of Key Vault managed Azure Storage Account and sets the key as the active key.</span></span> <span data-ttu-id="ca42c-107">Прокси-сервер хранилища ключей. вызов в диспетчере ресурсов Azure для повторного создания ключа.</span><span class="sxs-lookup"><span data-stu-id="ca42c-107">Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span></span> <span data-ttu-id="ca42c-108">Вызывающий объект должен posses разрешения на повторное создание ключей в указанной учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="ca42c-108">The caller must posses permissions to regenerate keys on given Azure Storage Account.</span></span>

## <span data-ttu-id="ca42c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ca42c-109">EXAMPLES</span></span>

### <span data-ttu-id="ca42c-110">Пример 1: повторное создание ключа</span><span class="sxs-lookup"><span data-stu-id="ca42c-110">Example 1: Regenerate a key</span></span>
```
PS C:\> Update-AzKeyVaultManagedStorageAccountKey -VaultName 'myvault' -AccountName 'mystorageaccount' -KeyName 'key1'
```

<span data-ttu-id="ca42c-111">Повторное создание "key1" учетной записи "mystorageaccount" и установка "key1" в качестве активной учетной записи хранения для хранилища ключей в службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="ca42c-111">Regenerates 'key1' of account 'mystorageaccount' and sets 'key1' as the active of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="ca42c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ca42c-112">PARAMETERS</span></span>

### <span data-ttu-id="ca42c-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="ca42c-113">-AccountName</span></span>
<span data-ttu-id="ca42c-114">Имя учетной записи хранилища с управляемым хранилищем.</span><span class="sxs-lookup"><span data-stu-id="ca42c-114">Key Vault managed storage account name.</span></span> <span data-ttu-id="ca42c-115">Командлет создает полное доменное имя управляемой учетной записи хранения из имени хранилища, выбранной в данный момент среды и управляемого имени учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="ca42c-115">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="ca42c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca42c-116">-DefaultProfile</span></span>
<span data-ttu-id="ca42c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ca42c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca42c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ca42c-118">-Force</span></span>
<span data-ttu-id="ca42c-119">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="ca42c-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ca42c-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="ca42c-120">-KeyName</span></span>
<span data-ttu-id="ca42c-121">Имя ключа учетной записи хранения, которое нужно повторно создать и сделать активным.</span><span class="sxs-lookup"><span data-stu-id="ca42c-121">Name of storage account key to regenerate and make active.</span></span>

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

### <span data-ttu-id="ca42c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca42c-122">-PassThru</span></span>
<span data-ttu-id="ca42c-123">По умолчанию командлет не возвращает объект.</span><span class="sxs-lookup"><span data-stu-id="ca42c-123">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="ca42c-124">Если этот параметр указан, командлет возвращает управляемую учетную запись хранения, которая была удалена.</span><span class="sxs-lookup"><span data-stu-id="ca42c-124">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="ca42c-125">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ca42c-125">-VaultName</span></span>
<span data-ttu-id="ca42c-126">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="ca42c-126">Vault name.</span></span>
<span data-ttu-id="ca42c-127">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="ca42c-127">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="ca42c-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ca42c-128">-Confirm</span></span>
<span data-ttu-id="ca42c-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ca42c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca42c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca42c-130">-WhatIf</span></span>
<span data-ttu-id="ca42c-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ca42c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca42c-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ca42c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca42c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca42c-133">CommonParameters</span></span>
<span data-ttu-id="ca42c-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ca42c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca42c-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca42c-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca42c-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ca42c-136">INPUTS</span></span>

### <span data-ttu-id="ca42c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="ca42c-137">System.String</span></span>

## <span data-ttu-id="ca42c-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca42c-138">OUTPUTS</span></span>

### <span data-ttu-id="ca42c-139">Microsoft. Azure. Commands. KeyVault. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ca42c-139">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="ca42c-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="ca42c-140">NOTES</span></span>

## <span data-ttu-id="ca42c-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ca42c-141">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

