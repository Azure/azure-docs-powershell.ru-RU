---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 47383ee57d527f6348781e57ed965e1ed8d36ef2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93911755"
---
# <span data-ttu-id="b116c-101">New-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="b116c-101">New-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="b116c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b116c-102">SYNOPSIS</span></span>
<span data-ttu-id="b116c-103">Создает новый снимок NetApp файлов Azure (ANF).</span><span class="sxs-lookup"><span data-stu-id="b116c-103">Creates a new Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="b116c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b116c-104">SYNTAX</span></span>

### <span data-ttu-id="b116c-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b116c-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesSnapshot -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -VolumeName <String> -Name <String> [-FileSystemId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b116c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b116c-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesSnapshot -Name <String> [-Tag <Hashtable>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b116c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b116c-107">DESCRIPTION</span></span>
<span data-ttu-id="b116c-108">Командлет **New-AzNetAppFilesSnapshot** создает моментальный снимок ANF.</span><span class="sxs-lookup"><span data-stu-id="b116c-108">The **New-AzNetAppFilesSnapshot** cmdlet creates an ANF snapshot.</span></span>

## <span data-ttu-id="b116c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b116c-109">EXAMPLES</span></span>

### <span data-ttu-id="b116c-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b116c-110">Example 1</span></span>
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

<span data-ttu-id="b116c-111">Эта команда создает новый снимок ANF "MyAnfSnapshot" в томе "MyAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="b116c-111">This command creates the new ANF snapshot "MyAnfSnapshot" within the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="b116c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b116c-112">PARAMETERS</span></span>

### <span data-ttu-id="b116c-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="b116c-113">-AccountName</span></span>
<span data-ttu-id="b116c-114">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="b116c-114">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b116c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b116c-115">-DefaultProfile</span></span>
<span data-ttu-id="b116c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b116c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b116c-117">-FileSystemId</span><span class="sxs-lookup"><span data-stu-id="b116c-117">-FileSystemId</span></span>
<span data-ttu-id="b116c-118">Идентификатор файловой системы</span><span class="sxs-lookup"><span data-stu-id="b116c-118">The file system id</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b116c-119">-Location</span><span class="sxs-lookup"><span data-stu-id="b116c-119">-Location</span></span>
<span data-ttu-id="b116c-120">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="b116c-120">The location of the resource</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b116c-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b116c-121">-Name</span></span>
<span data-ttu-id="b116c-122">Имя моментального снимка ANF</span><span class="sxs-lookup"><span data-stu-id="b116c-122">The name of the ANF snapshot</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SnapshotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b116c-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="b116c-123">-PoolName</span></span>
<span data-ttu-id="b116c-124">Название пула ANF</span><span class="sxs-lookup"><span data-stu-id="b116c-124">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b116c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b116c-125">-ResourceGroupName</span></span>
<span data-ttu-id="b116c-126">Группа ресурсов для учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="b116c-126">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b116c-127">-Тег</span><span class="sxs-lookup"><span data-stu-id="b116c-127">-Tag</span></span>
<span data-ttu-id="b116c-128">Хэш-таблица, представляющая Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="b116c-128">A hashtable which represents resource tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b116c-129">-Тома</span><span class="sxs-lookup"><span data-stu-id="b116c-129">-VolumeName</span></span>
<span data-ttu-id="b116c-130">Имя ANFого тома.</span><span class="sxs-lookup"><span data-stu-id="b116c-130">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b116c-131">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="b116c-131">-VolumeObject</span></span>
<span data-ttu-id="b116c-132">Громкость нового объекта Snapshot</span><span class="sxs-lookup"><span data-stu-id="b116c-132">The volume for the new snapshot object</span></span>

```yaml
Type: PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b116c-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b116c-133">-Confirm</span></span>
<span data-ttu-id="b116c-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b116c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b116c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b116c-135">-WhatIf</span></span>
<span data-ttu-id="b116c-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b116c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b116c-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b116c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b116c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b116c-138">CommonParameters</span></span>
<span data-ttu-id="b116c-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b116c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b116c-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b116c-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b116c-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b116c-141">INPUTS</span></span>

### <span data-ttu-id="b116c-142">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="b116c-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="b116c-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b116c-143">OUTPUTS</span></span>

### <span data-ttu-id="b116c-144">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="b116c-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="b116c-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="b116c-145">NOTES</span></span>

## <span data-ttu-id="b116c-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b116c-146">RELATED LINKS</span></span>
