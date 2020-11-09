---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstoragefileserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageFileServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageFileServiceProperty.md
ms.openlocfilehash: e0e4eefaa652ca47f2d397acee1eeb0c8806de76
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318308"
---
# <span data-ttu-id="b6f72-101">Update-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="b6f72-101">Update-AzStorageFileServiceProperty</span></span>

## <span data-ttu-id="b6f72-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b6f72-102">SYNOPSIS</span></span>
<span data-ttu-id="b6f72-103">Изменение свойств службы в службе файлов хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="b6f72-103">Modifies the service properties for the Azure Storage File service.</span></span>

## <span data-ttu-id="b6f72-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b6f72-104">SYNTAX</span></span>

### <span data-ttu-id="b6f72-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b6f72-105">AccountName (Default)</span></span>
```
Update-AzStorageFileServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-EnableShareDeleteRetentionPolicy <Boolean>] [-ShareRetentionDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6f72-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="b6f72-106">AccountObject</span></span>
```
Update-AzStorageFileServiceProperty -StorageAccount <PSStorageAccount>
 [-EnableShareDeleteRetentionPolicy <Boolean>] [-ShareRetentionDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6f72-107">FileServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="b6f72-107">FileServicePropertiesResourceId</span></span>
```
Update-AzStorageFileServiceProperty [-ResourceId] <String> [-EnableShareDeleteRetentionPolicy <Boolean>]
 [-ShareRetentionDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b6f72-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6f72-108">DESCRIPTION</span></span>
<span data-ttu-id="b6f72-109">Командлет **Update-AzStorageFileServiceProperty** изменяет свойства службы хранения файлов Azure.</span><span class="sxs-lookup"><span data-stu-id="b6f72-109">The **Update-AzStorageFileServiceProperty** cmdlet modifies the service properties for the Azure Storage File service.</span></span>

## <span data-ttu-id="b6f72-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b6f72-110">EXAMPLES</span></span>

### <span data-ttu-id="b6f72-111">Пример 1: Включение общего доступа к файлам softdelete</span><span class="sxs-lookup"><span data-stu-id="b6f72-111">Example 1: Enable File share softdelete</span></span>
```powershell
PS C:\> Update-AzStorageFileServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EnableShareDeleteRetentionPolicy $true -ShareRetentionDays 5

StorageAccountName ResourceGroupName ShareDeleteRetentionPolicy.Enabled ShareDeleteRetentionPolicy.Days
------------------ ----------------- ---------------------------------- -------------------------------
mystorageaccount   myresourcegroup   True                               5
```

<span data-ttu-id="b6f72-112">Эта команда включает softdelete "общий доступ к файлам" с днями хранения как 5</span><span class="sxs-lookup"><span data-stu-id="b6f72-112">This command enables File share softdelete delete with retention days as 5</span></span>

## <span data-ttu-id="b6f72-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b6f72-113">PARAMETERS</span></span>

### <span data-ttu-id="b6f72-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6f72-114">-DefaultProfile</span></span>
<span data-ttu-id="b6f72-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b6f72-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6f72-116">-EnableShareDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b6f72-116">-EnableShareDeleteRetentionPolicy</span></span>
<span data-ttu-id="b6f72-117">Включите общий доступ удаление политики хранения для учетной записи хранения, выбрав значение $true, отключите параметр Общий доступ удаление политики хранения с помощью значения $false.</span><span class="sxs-lookup"><span data-stu-id="b6f72-117">Enable share Delete Retention Policy for the storage account by set to $true, disable share Delete Retention Policy  by set to $false.</span></span>

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

### <span data-ttu-id="b6f72-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6f72-118">-ResourceGroupName</span></span>
<span data-ttu-id="b6f72-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b6f72-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="b6f72-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6f72-120">-ResourceId</span></span>
<span data-ttu-id="b6f72-121">Введите идентификатор ресурса учетной записи хранилища или идентификатор ресурса свойств службы файлов.</span><span class="sxs-lookup"><span data-stu-id="b6f72-121">Input a Storage account Resource Id, or a File service properties Resource Id.</span></span>

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

### <span data-ttu-id="b6f72-122">-ShareRetentionDays</span><span class="sxs-lookup"><span data-stu-id="b6f72-122">-ShareRetentionDays</span></span>
<span data-ttu-id="b6f72-123">Задает количество дней хранения для DeleteRetentionPolicy общего доступа.</span><span class="sxs-lookup"><span data-stu-id="b6f72-123">Sets the number of retention days for the share DeleteRetentionPolicy.</span></span>
<span data-ttu-id="b6f72-124">Значение должно быть установлено только в том случае, если параметр Включить общий доступ удаление политики хранения.</span><span class="sxs-lookup"><span data-stu-id="b6f72-124">The value should only be set when enable share Delete Retention Policy.</span></span>

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

### <span data-ttu-id="b6f72-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="b6f72-125">-StorageAccount</span></span>
<span data-ttu-id="b6f72-126">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="b6f72-126">Storage account object</span></span>

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

### <span data-ttu-id="b6f72-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b6f72-127">-StorageAccountName</span></span>
<span data-ttu-id="b6f72-128">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="b6f72-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="b6f72-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6f72-129">-Confirm</span></span>
<span data-ttu-id="b6f72-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b6f72-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6f72-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6f72-131">-WhatIf</span></span>
<span data-ttu-id="b6f72-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b6f72-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6f72-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b6f72-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6f72-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6f72-134">CommonParameters</span></span>
<span data-ttu-id="b6f72-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b6f72-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6f72-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6f72-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6f72-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b6f72-137">INPUTS</span></span>

### <span data-ttu-id="b6f72-138">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b6f72-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="b6f72-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b6f72-139">System.String</span></span>

## <span data-ttu-id="b6f72-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6f72-140">OUTPUTS</span></span>

### <span data-ttu-id="b6f72-141">Microsoft. Azure. Commands. Management. Storage. Models. PSFileServiceProperties</span><span class="sxs-lookup"><span data-stu-id="b6f72-141">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span></span>

## <span data-ttu-id="b6f72-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="b6f72-142">NOTES</span></span>

## <span data-ttu-id="b6f72-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b6f72-143">RELATED LINKS</span></span>