---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstoragefileserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageFileServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageFileServiceProperty.md
ms.openlocfilehash: e0e4eefaa652ca47f2d397acee1eeb0c8806de76
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100231537"
---
# <span data-ttu-id="23e97-101">Update-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="23e97-101">Update-AzStorageFileServiceProperty</span></span>

## <span data-ttu-id="23e97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23e97-102">SYNOPSIS</span></span>
<span data-ttu-id="23e97-103">Изменяет свойства службы для службы файлов хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="23e97-103">Modifies the service properties for the Azure Storage File service.</span></span>

## <span data-ttu-id="23e97-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="23e97-104">SYNTAX</span></span>

### <span data-ttu-id="23e97-105">AccountName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="23e97-105">AccountName (Default)</span></span>
```
Update-AzStorageFileServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-EnableShareDeleteRetentionPolicy <Boolean>] [-ShareRetentionDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23e97-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="23e97-106">AccountObject</span></span>
```
Update-AzStorageFileServiceProperty -StorageAccount <PSStorageAccount>
 [-EnableShareDeleteRetentionPolicy <Boolean>] [-ShareRetentionDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23e97-107">FileServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="23e97-107">FileServicePropertiesResourceId</span></span>
```
Update-AzStorageFileServiceProperty [-ResourceId] <String> [-EnableShareDeleteRetentionPolicy <Boolean>]
 [-ShareRetentionDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="23e97-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="23e97-108">DESCRIPTION</span></span>
<span data-ttu-id="23e97-109">Для службы файлов хранилища Azure свойства службы **Update-AzStorageFileServiceProperty** изменяется.</span><span class="sxs-lookup"><span data-stu-id="23e97-109">The **Update-AzStorageFileServiceProperty** cmdlet modifies the service properties for the Azure Storage File service.</span></span>

## <span data-ttu-id="23e97-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="23e97-110">EXAMPLES</span></span>

### <span data-ttu-id="23e97-111">Пример 1. Enable File share softdelete</span><span class="sxs-lookup"><span data-stu-id="23e97-111">Example 1: Enable File share softdelete</span></span>
```powershell
PS C:\> Update-AzStorageFileServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EnableShareDeleteRetentionPolicy $true -ShareRetentionDays 5

StorageAccountName ResourceGroupName ShareDeleteRetentionPolicy.Enabled ShareDeleteRetentionPolicy.Days
------------------ ----------------- ---------------------------------- -------------------------------
mystorageaccount   myresourcegroup   True                               5
```

<span data-ttu-id="23e97-112">Эта команда позволяет делиться файлами со softdelete удалить, при этом срок хранения составляет 5 дней.</span><span class="sxs-lookup"><span data-stu-id="23e97-112">This command enables File share softdelete delete with retention days as 5</span></span>

## <span data-ttu-id="23e97-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23e97-113">PARAMETERS</span></span>

### <span data-ttu-id="23e97-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23e97-114">-DefaultProfile</span></span>
<span data-ttu-id="23e97-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="23e97-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e97-116">-EnableShareDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="23e97-116">-EnableShareDeleteRetentionPolicy</span></span>
<span data-ttu-id="23e97-117">Включите совместное хранение для учетной записи хранения, заключив для нее $true, отключите политику хранения удаления, заключив для нее $false.</span><span class="sxs-lookup"><span data-stu-id="23e97-117">Enable share Delete Retention Policy for the storage account by set to $true, disable share Delete Retention Policy  by set to $false.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e97-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23e97-118">-ResourceGroupName</span></span>
<span data-ttu-id="23e97-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="23e97-119">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e97-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23e97-120">-ResourceId</span></span>
<span data-ttu-id="23e97-121">Ввести ИД ресурса учетной записи хранения или свойства ресурса службы файлов.</span><span class="sxs-lookup"><span data-stu-id="23e97-121">Input a Storage account Resource Id, or a File service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: FileServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23e97-122">-ShareRetentionDays</span><span class="sxs-lookup"><span data-stu-id="23e97-122">-ShareRetentionDays</span></span>
<span data-ttu-id="23e97-123">Определяет количество дней хранения для share DeleteRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="23e97-123">Sets the number of retention days for the share DeleteRetentionPolicy.</span></span>
<span data-ttu-id="23e97-124">Это значение следует устанавливать только в том случае, если включить совместное хранение удаления.</span><span class="sxs-lookup"><span data-stu-id="23e97-124">The value should only be set when enable share Delete Retention Policy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Days, RetentionDays

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e97-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="23e97-125">-StorageAccount</span></span>
<span data-ttu-id="23e97-126">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="23e97-126">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23e97-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="23e97-127">-StorageAccountName</span></span>
<span data-ttu-id="23e97-128">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="23e97-128">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e97-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="23e97-129">-Confirm</span></span>
<span data-ttu-id="23e97-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="23e97-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23e97-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23e97-131">-WhatIf</span></span>
<span data-ttu-id="23e97-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23e97-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23e97-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="23e97-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23e97-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23e97-134">CommonParameters</span></span>
<span data-ttu-id="23e97-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23e97-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23e97-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23e97-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23e97-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="23e97-137">INPUTS</span></span>

### <span data-ttu-id="23e97-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="23e97-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="23e97-139">System.String</span><span class="sxs-lookup"><span data-stu-id="23e97-139">System.String</span></span>

## <span data-ttu-id="23e97-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="23e97-140">OUTPUTS</span></span>

### <span data-ttu-id="23e97-141">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span><span class="sxs-lookup"><span data-stu-id="23e97-141">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span></span>

## <span data-ttu-id="23e97-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="23e97-142">NOTES</span></span>

## <span data-ttu-id="23e97-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="23e97-143">RELATED LINKS</span></span>
