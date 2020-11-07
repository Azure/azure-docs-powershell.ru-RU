---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeShare.md
ms.openlocfilehash: 19dd22f15400e99f95947d97fe8c46077911de61
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911269"
---
# <span data-ttu-id="28c19-101">New-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="28c19-101">New-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="28c19-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="28c19-102">SYNOPSIS</span></span>
<span data-ttu-id="28c19-103">Создание нового общего доступа на устройстве.</span><span class="sxs-lookup"><span data-stu-id="28c19-103">Creates a new share on the device.</span></span>

## <span data-ttu-id="28c19-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="28c19-104">SYNTAX</span></span>

### <span data-ttu-id="28c19-105">SmbParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="28c19-105">SmbParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="28c19-106">CloudShareNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="28c19-106">CloudShareNfsParameterSet</span></span>
```
New-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="28c19-107">CloudShareSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="28c19-107">CloudShareSmbParameterSet</span></span>
```
New-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="28c19-108">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="28c19-108">NfsParameterSet</span></span>
```
New-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="28c19-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="28c19-109">DESCRIPTION</span></span>
<span data-ttu-id="28c19-110">Командлет **New-AzDataBoxEdgeShare** создает новый общий доступ на пограничном устройстве поля данных.</span><span class="sxs-lookup"><span data-stu-id="28c19-110">The **New-AzDataBoxEdgeShare** cmdlet creates a new share on the Data Box Edge device.</span></span>

## <span data-ttu-id="28c19-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="28c19-111">EXAMPLES</span></span>

### <span data-ttu-id="28c19-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="28c19-112">Example 1</span></span>
```
PS C:\> New-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share-1 -SMB
-StorageAccountCredentialName storageCredentialName -DataFormat PageBlob
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="28c19-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="28c19-113">PARAMETERS</span></span>

### <span data-ttu-id="28c19-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="28c19-114">-AsJob</span></span>
<span data-ttu-id="28c19-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="28c19-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="28c19-116">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="28c19-116">-ClientAccessRight</span></span>
<span data-ttu-id="28c19-117">Доступ для чтения и записи для clientId, для ex: @ (@ {"ClientId" = "192.168.10.10"; " AccessRight "=" недоступен "}, @ {" ClientId "=" 192.168.10.11 ";" AccessRight "=" только для чтения "})</span><span class="sxs-lookup"><span data-stu-id="28c19-117">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: CloudShareNfsParameterSet, NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28c19-118">-CloudShare</span><span class="sxs-lookup"><span data-stu-id="28c19-118">-CloudShare</span></span>
<span data-ttu-id="28c19-119">Укажите имя ресурса для существующего StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="28c19-119">Provide existing StorageAccountCredential's Resource Name</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28c19-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="28c19-120">-ContainerName</span></span>
<span data-ttu-id="28c19-121">Имя контейнера (на основе указанного формата данных — это имя файла Azure/Pageblob/Block BLOB).</span><span class="sxs-lookup"><span data-stu-id="28c19-121">Container name (Based on the data format specified, this represents the name of Azure Files/Pageblob/Block blob)</span></span>

```yaml
Type: System.String
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28c19-122">-Формат.</span><span class="sxs-lookup"><span data-stu-id="28c19-122">-DataFormat</span></span>
<span data-ttu-id="28c19-123">Настройка формата данных ex: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="28c19-123">Set Data Format ex: PageBlob, BlobBlob</span></span>

```yaml
Type: System.String
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28c19-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28c19-124">-DefaultProfile</span></span>
<span data-ttu-id="28c19-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="28c19-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28c19-126">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="28c19-126">-DeviceName</span></span>
<span data-ttu-id="28c19-127">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="28c19-127">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28c19-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="28c19-128">-Name</span></span>
<span data-ttu-id="28c19-129">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="28c19-129">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28c19-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="28c19-130">-NFS</span></span>
<span data-ttu-id="28c19-131">AccessProtocol в случае создания общего доступа</span><span class="sxs-lookup"><span data-stu-id="28c19-131">AccessProtocol in the case of creating Share</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CloudShareNfsParameterSet, NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28c19-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28c19-132">-ResourceGroupName</span></span>
<span data-ttu-id="28c19-133">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="28c19-133">Resource Group Name</span></span>

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

### <span data-ttu-id="28c19-134">-SMB</span><span class="sxs-lookup"><span data-stu-id="28c19-134">-SMB</span></span>
<span data-ttu-id="28c19-135">AccessProtocol в случае создания общего доступа</span><span class="sxs-lookup"><span data-stu-id="28c19-135">AccessProtocol in the case of creating Share</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SmbParameterSet, CloudShareSmbParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28c19-136">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="28c19-136">-StorageAccountCredentialName</span></span>
<span data-ttu-id="28c19-137">Укажите имя ресурса для существующего StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="28c19-137">Provide existing StorageAccountCredential's Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28c19-138">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="28c19-138">-UserAccessRight</span></span>
<span data-ttu-id="28c19-139">Предоставьте право доступа вместе с существующими именами пользователей для доступа к типам общего доступа к SMB, например: @ (@ {"Username" = "User-Name-1"; " AccessRight "=" Read "}, @ {" ИмяПользователя "=" User-Name-2 ";" AccessRight "=" Read "}, @ {" ИмяПользователя "=" User-Name-3 ";" AccessRight "=" Custom "})</span><span class="sxs-lookup"><span data-stu-id="28c19-139">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: SmbParameterSet, CloudShareSmbParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28c19-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="28c19-140">-Confirm</span></span>
<span data-ttu-id="28c19-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="28c19-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28c19-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28c19-142">-WhatIf</span></span>
<span data-ttu-id="28c19-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="28c19-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="28c19-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="28c19-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28c19-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28c19-145">CommonParameters</span></span>
<span data-ttu-id="28c19-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="28c19-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28c19-147">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28c19-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28c19-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="28c19-148">INPUTS</span></span>

### <span data-ttu-id="28c19-149">System. String</span><span class="sxs-lookup"><span data-stu-id="28c19-149">System.String</span></span>

## <span data-ttu-id="28c19-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="28c19-150">OUTPUTS</span></span>

### <span data-ttu-id="28c19-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="28c19-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="28c19-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="28c19-152">NOTES</span></span>

## <span data-ttu-id="28c19-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="28c19-153">RELATED LINKS</span></span>
