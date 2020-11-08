---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 1fe8da5c9ee899b7aa1a77a9fbb0ac7a2bf3b35c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244168"
---
# <span data-ttu-id="2ea06-101">New-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="2ea06-101">New-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="2ea06-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2ea06-102">SYNOPSIS</span></span>
<span data-ttu-id="2ea06-103">Создает новый снимок NetApp файлов Azure (ANF).</span><span class="sxs-lookup"><span data-stu-id="2ea06-103">Creates a new Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="2ea06-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2ea06-104">SYNTAX</span></span>

### <span data-ttu-id="2ea06-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2ea06-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesSnapshot -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -VolumeName <String> -Name <String> [-FileSystemId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ea06-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ea06-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesSnapshot -Name <String> [-Tag <Hashtable>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ea06-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ea06-107">DESCRIPTION</span></span>
<span data-ttu-id="2ea06-108">Командлет **New-AzNetAppFilesSnapshot** создает моментальный снимок ANF.</span><span class="sxs-lookup"><span data-stu-id="2ea06-108">The **New-AzNetAppFilesSnapshot** cmdlet creates an ANF snapshot.</span></span>

## <span data-ttu-id="2ea06-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2ea06-109">EXAMPLES</span></span>

### <span data-ttu-id="2ea06-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2ea06-110">Example 1</span></span>
```
PS C:\>New-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -SnapshotName "MyAnfSnapshot" -FileSystemId "3e2773a7-2a72-d003-0637-1a8b1fa3eaaf"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume/snapshots/MyAnfSnapshot
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume/MyAnfSnapshot
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes/snapshots
Tags              :
SnapshotId        : ca7c4ebd-91cb-0e30-91f5-9154050033df
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
Created           :
ProvisioningState : Succeeded
```

<span data-ttu-id="2ea06-111">Эта команда создает новый снимок ANF "MyAnfSnapshot" в томе "MyAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="2ea06-111">This command creates the new ANF snapshot "MyAnfSnapshot" within the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="2ea06-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2ea06-112">PARAMETERS</span></span>

### <span data-ttu-id="2ea06-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="2ea06-113">-AccountName</span></span>
<span data-ttu-id="2ea06-114">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="2ea06-114">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ea06-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ea06-115">-DefaultProfile</span></span>
<span data-ttu-id="2ea06-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2ea06-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ea06-117">-FileSystemId</span><span class="sxs-lookup"><span data-stu-id="2ea06-117">-FileSystemId</span></span>
<span data-ttu-id="2ea06-118">Идентификатор файловой системы</span><span class="sxs-lookup"><span data-stu-id="2ea06-118">The file system id</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ea06-119">-Location</span><span class="sxs-lookup"><span data-stu-id="2ea06-119">-Location</span></span>
<span data-ttu-id="2ea06-120">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="2ea06-120">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ea06-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2ea06-121">-Name</span></span>
<span data-ttu-id="2ea06-122">Имя моментального снимка ANF</span><span class="sxs-lookup"><span data-stu-id="2ea06-122">The name of the ANF snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SnapshotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ea06-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="2ea06-123">-PoolName</span></span>
<span data-ttu-id="2ea06-124">Название пула ANF</span><span class="sxs-lookup"><span data-stu-id="2ea06-124">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ea06-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ea06-125">-ResourceGroupName</span></span>
<span data-ttu-id="2ea06-126">Группа ресурсов для учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="2ea06-126">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ea06-127">-Тег</span><span class="sxs-lookup"><span data-stu-id="2ea06-127">-Tag</span></span>
<span data-ttu-id="2ea06-128">Хэш-таблица, представляющая Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="2ea06-128">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ea06-129">-Тома</span><span class="sxs-lookup"><span data-stu-id="2ea06-129">-VolumeName</span></span>
<span data-ttu-id="2ea06-130">Имя ANFого тома.</span><span class="sxs-lookup"><span data-stu-id="2ea06-130">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ea06-131">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="2ea06-131">-VolumeObject</span></span>
<span data-ttu-id="2ea06-132">Громкость нового объекта Snapshot</span><span class="sxs-lookup"><span data-stu-id="2ea06-132">The volume for the new snapshot object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ea06-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2ea06-133">-Confirm</span></span>
<span data-ttu-id="2ea06-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2ea06-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ea06-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ea06-135">-WhatIf</span></span>
<span data-ttu-id="2ea06-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2ea06-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ea06-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2ea06-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ea06-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ea06-138">CommonParameters</span></span>
<span data-ttu-id="2ea06-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2ea06-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ea06-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2ea06-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ea06-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2ea06-141">INPUTS</span></span>

### <span data-ttu-id="2ea06-142">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="2ea06-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="2ea06-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ea06-143">OUTPUTS</span></span>

### <span data-ttu-id="2ea06-144">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="2ea06-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="2ea06-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="2ea06-145">NOTES</span></span>

## <span data-ttu-id="2ea06-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2ea06-146">RELATED LINKS</span></span>
