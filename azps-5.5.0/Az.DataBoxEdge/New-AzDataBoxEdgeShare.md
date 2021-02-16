---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeShare.md
ms.openlocfilehash: 23dcfa42b1b7821e7d2c47b7b3c5e7d7b8579ed6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242856"
---
# <span data-ttu-id="30865-101">New-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="30865-101">New-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="30865-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30865-102">SYNOPSIS</span></span>
<span data-ttu-id="30865-103">Создает новую обетовую долю на устройстве.</span><span class="sxs-lookup"><span data-stu-id="30865-103">Creates a new share on the device.</span></span>

## <span data-ttu-id="30865-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="30865-104">SYNTAX</span></span>

### <span data-ttu-id="30865-105">SmbParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="30865-105">SmbParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="30865-106">CloudShareNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="30865-106">CloudShareNfsParameterSet</span></span>
```
New-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="30865-107">CloudShareSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="30865-107">CloudShareSmbParameterSet</span></span>
```
New-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="30865-108">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="30865-108">NfsParameterSet</span></span>
```
New-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="30865-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="30865-109">DESCRIPTION</span></span>
<span data-ttu-id="30865-110">С **новыми данными AzDataBoxEdgeShare** на устройстве Edge box данных создается новая обилие.</span><span class="sxs-lookup"><span data-stu-id="30865-110">The **New-AzDataBoxEdgeShare** cmdlet creates a new share on the Data Box Edge device.</span></span>

## <span data-ttu-id="30865-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="30865-111">EXAMPLES</span></span>

### <span data-ttu-id="30865-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="30865-112">Example 1</span></span>
```
PS C:\> New-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share-1 -SMB
-StorageAccountCredentialName storageCredentialName -DataFormat PageBlob
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="30865-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30865-113">PARAMETERS</span></span>

### <span data-ttu-id="30865-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30865-114">-AsJob</span></span>
<span data-ttu-id="30865-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="30865-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="30865-116">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="30865-116">-ClientAccessRight</span></span>
<span data-ttu-id="30865-117">Read/Write Access for clientIds, for ex:@(@{"ClientId"="192.168.10.10";" AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";" AccessRight"="ReadOnly"})</span><span class="sxs-lookup"><span data-stu-id="30865-117">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

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

### <span data-ttu-id="30865-118">-CloudShare</span><span class="sxs-lookup"><span data-stu-id="30865-118">-CloudShare</span></span>
<span data-ttu-id="30865-119">Укайм существующее имя ресурса StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="30865-119">Provide existing StorageAccountCredential's Resource Name</span></span>

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

### <span data-ttu-id="30865-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="30865-120">-ContainerName</span></span>
<span data-ttu-id="30865-121">Имя контейнера (в зависимости от заданного формата данных, это имя azure Files/Pageblob/Block BLOB-файла)</span><span class="sxs-lookup"><span data-stu-id="30865-121">Container name (Based on the data format specified, this represents the name of Azure Files/Pageblob/Block blob)</span></span>

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

### <span data-ttu-id="30865-122">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="30865-122">-DataFormat</span></span>
<span data-ttu-id="30865-123">Set Data Format ex: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="30865-123">Set Data Format ex: PageBlob, BlobBlob</span></span>

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

### <span data-ttu-id="30865-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30865-124">-DefaultProfile</span></span>
<span data-ttu-id="30865-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="30865-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30865-126">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="30865-126">-DeviceName</span></span>
<span data-ttu-id="30865-127">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="30865-127">Device Name</span></span>

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

### <span data-ttu-id="30865-128">-Name</span><span class="sxs-lookup"><span data-stu-id="30865-128">-Name</span></span>
<span data-ttu-id="30865-129">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="30865-129">Resource Name</span></span>

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

### <span data-ttu-id="30865-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="30865-130">-NFS</span></span>
<span data-ttu-id="30865-131">AccessProtocol в случае создания "Поделиться"</span><span class="sxs-lookup"><span data-stu-id="30865-131">AccessProtocol in the case of creating Share</span></span>

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

### <span data-ttu-id="30865-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30865-132">-ResourceGroupName</span></span>
<span data-ttu-id="30865-133">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="30865-133">Resource Group Name</span></span>

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

### <span data-ttu-id="30865-134">-SMB</span><span class="sxs-lookup"><span data-stu-id="30865-134">-SMB</span></span>
<span data-ttu-id="30865-135">AccessProtocol в случае создания "Поделиться"</span><span class="sxs-lookup"><span data-stu-id="30865-135">AccessProtocol in the case of creating Share</span></span>

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

### <span data-ttu-id="30865-136">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="30865-136">-StorageAccountCredentialName</span></span>
<span data-ttu-id="30865-137">Укайм существующее имя ресурса StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="30865-137">Provide existing StorageAccountCredential's Resource Name</span></span>

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

### <span data-ttu-id="30865-138">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="30865-138">-UserAccessRight</span></span>
<span data-ttu-id="30865-139">предоставить доступ прямо вместе с существующими именами пользователей для доступа к типам "Общий доступ К SMB", например: @(@{"Имя пользователя"="имя пользователя-1";" AccessRight"="Read"}, @{"Username"="user-name-2";" AccessRight"="Read"}, @{"Username"="user-name-3";" AccessRight"="Custom"})</span><span class="sxs-lookup"><span data-stu-id="30865-139">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

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

### <span data-ttu-id="30865-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="30865-140">-Confirm</span></span>
<span data-ttu-id="30865-141">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30865-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30865-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30865-142">-WhatIf</span></span>
<span data-ttu-id="30865-143">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30865-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="30865-144">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="30865-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30865-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30865-145">CommonParameters</span></span>
<span data-ttu-id="30865-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30865-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30865-147">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30865-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30865-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="30865-148">INPUTS</span></span>

### <span data-ttu-id="30865-149">System.String</span><span class="sxs-lookup"><span data-stu-id="30865-149">System.String</span></span>

## <span data-ttu-id="30865-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="30865-150">OUTPUTS</span></span>

### <span data-ttu-id="30865-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="30865-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="30865-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="30865-152">NOTES</span></span>

## <span data-ttu-id="30865-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="30865-153">RELATED LINKS</span></span>
