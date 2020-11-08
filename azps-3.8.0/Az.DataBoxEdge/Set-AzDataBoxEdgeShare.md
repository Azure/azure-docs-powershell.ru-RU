---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeShare.md
ms.openlocfilehash: 8bef754d7d9020193e4694953222a6579341c9ed
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073842"
---
# <span data-ttu-id="c3d4a-101">Set-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="c3d4a-101">Set-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="c3d4a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c3d4a-102">SYNOPSIS</span></span>
<span data-ttu-id="c3d4a-103">Обновление общего доступа для устройства.</span><span class="sxs-lookup"><span data-stu-id="c3d4a-103">Updates the share for a device.</span></span>

## <span data-ttu-id="c3d4a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c3d4a-104">SYNTAX</span></span>

### <span data-ttu-id="c3d4a-105">SmbParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c3d4a-105">SmbParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -UserAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c3d4a-106">UpdateByResourceIdSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3d4a-106">UpdateByResourceIdSmbParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -ResourceId <String> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3d4a-107">UpdateByResourceIdNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3d4a-107">UpdateByResourceIdNfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -ResourceId <String> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3d4a-108">UpdateByInputObjectSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3d4a-108">UpdateByInputObjectSmbParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -InputObject <PSDataBoxEdgeShare> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3d4a-109">UpdateByInputObjectNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3d4a-109">UpdateByInputObjectNfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -InputObject <PSDataBoxEdgeShare> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3d4a-110">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3d4a-110">NfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -ClientAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c3d4a-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c3d4a-111">DESCRIPTION</span></span>
<span data-ttu-id="c3d4a-112">Этот **Set-AzDataBoxEdgeShare** заменит права доступа</span><span class="sxs-lookup"><span data-stu-id="c3d4a-112">This **Set-AzDataBoxEdgeShare** will replace the access rights</span></span>

## <span data-ttu-id="c3d4a-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c3d4a-113">EXAMPLES</span></span>

### <span data-ttu-id="c3d4a-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c3d4a-114">Example 1</span></span>
```powershell
PS C:\> $AccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
PS C:\> Set-AzDataBoxEdgeShare -ResourceGroupName resource-group-name -ClientAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-2    NFS        Cloud            PageBlob         resource-group-name   storage-account-name
## $ClientAccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
## Possible values for AccessRight options are 'NoAccess', 'ReadOnly', 'ReadWrite'
```

### <span data-ttu-id="c3d4a-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c3d4a-115">Example 2</span></span>
```powershell
PS C:\> $AccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
PS C:\> Set-AzDataBoxEdgeShare -ResourceGroupName resource-group-name -UserAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resource-group-name   storage-account-name
## $UserAccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
## Possible values for AccessRight are 'Change', 'Read', 'Custom'
```

## <span data-ttu-id="c3d4a-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c3d4a-116">PARAMETERS</span></span>

### <span data-ttu-id="c3d4a-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3d4a-117">-AsJob</span></span>
<span data-ttu-id="c3d4a-118">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c3d4a-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c3d4a-119">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="c3d4a-119">-ClientAccessRight</span></span>
<span data-ttu-id="c3d4a-120">Доступ для чтения и записи для clientId, для ex: @ (@ {"ClientId" = "192.168.10.10"; " AccessRight "=" недоступен "}, @ {" ClientId "=" 192.168.10.11 ";" AccessRight "=" только для чтения "})</span><span class="sxs-lookup"><span data-stu-id="c3d4a-120">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: UpdateByResourceIdNfsParameterSet, UpdateByInputObjectNfsParameterSet, NfsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3d4a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3d4a-121">-DefaultProfile</span></span>
<span data-ttu-id="c3d4a-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c3d4a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3d4a-123">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="c3d4a-123">-DeviceName</span></span>
<span data-ttu-id="c3d4a-124">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="c3d4a-124">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3d4a-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3d4a-125">-InputObject</span></span>
<span data-ttu-id="c3d4a-126">Объект input</span><span class="sxs-lookup"><span data-stu-id="c3d4a-126">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare
Parameter Sets: UpdateByInputObjectSmbParameterSet, UpdateByInputObjectNfsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3d4a-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c3d4a-127">-Name</span></span>
<span data-ttu-id="c3d4a-128">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="c3d4a-128">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3d4a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3d4a-129">-ResourceGroupName</span></span>
<span data-ttu-id="c3d4a-130">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c3d4a-130">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3d4a-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3d4a-131">-ResourceId</span></span>
<span data-ttu-id="c3d4a-132">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3d4a-132">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdSmbParameterSet, UpdateByResourceIdNfsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3d4a-133">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="c3d4a-133">-UserAccessRight</span></span>
<span data-ttu-id="c3d4a-134">Предоставьте право доступа вместе с существующими именами пользователей для доступа к типам общего доступа к SMB, например: @ (@ {"Username" = "User-Name-1"; " AccessRight "=" Read "}, @ {" ИмяПользователя "=" User-Name-2 ";" AccessRight "=" Read "}, @ {" ИмяПользователя "=" User-Name-3 ";" AccessRight "=" Custom "})</span><span class="sxs-lookup"><span data-stu-id="c3d4a-134">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: SmbParameterSet, UpdateByResourceIdSmbParameterSet, UpdateByInputObjectSmbParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3d4a-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c3d4a-135">-Confirm</span></span>
<span data-ttu-id="c3d4a-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c3d4a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3d4a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3d4a-137">-WhatIf</span></span>
<span data-ttu-id="c3d4a-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c3d4a-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c3d4a-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c3d4a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3d4a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3d4a-140">CommonParameters</span></span>
<span data-ttu-id="c3d4a-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c3d4a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3d4a-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3d4a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3d4a-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c3d4a-143">INPUTS</span></span>

### <span data-ttu-id="c3d4a-144">System. String</span><span class="sxs-lookup"><span data-stu-id="c3d4a-144">System.String</span></span>

### <span data-ttu-id="c3d4a-145">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="c3d4a-145">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="c3d4a-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c3d4a-146">OUTPUTS</span></span>

### <span data-ttu-id="c3d4a-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="c3d4a-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="c3d4a-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="c3d4a-148">NOTES</span></span>

## <span data-ttu-id="c3d4a-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c3d4a-149">RELATED LINKS</span></span>
