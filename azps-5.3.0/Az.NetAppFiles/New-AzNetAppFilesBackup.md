---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackup.md
ms.openlocfilehash: 66ba63b3e350093173ae9d1badc6c717a3c682aa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505011"
---
# <span data-ttu-id="13b78-101">New-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="13b78-101">New-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="13b78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13b78-102">SYNOPSIS</span></span>
<span data-ttu-id="13b78-103">Создает новую резервную копию файлов Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="13b78-103">Creates a new Azure NetApp Files (ANF) backup.</span></span>

## <span data-ttu-id="13b78-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="13b78-104">SYNTAX</span></span>

### <span data-ttu-id="13b78-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="13b78-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesBackup -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> -Name <String> -Label <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13b78-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="13b78-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesBackup -Name <String> -Label <String> -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13b78-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="13b78-107">DESCRIPTION</span></span>
<span data-ttu-id="13b78-108">Для создания тома ANF создается резервная копия для **new-AzNetAppFilesBackup.**</span><span class="sxs-lookup"><span data-stu-id="13b78-108">The **New-AzNetAppFilesBackup** cmdlet creates a backup for an ANF volume.</span></span>

## <span data-ttu-id="13b78-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="13b78-109">EXAMPLES</span></span>

### <span data-ttu-id="13b78-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="13b78-110">Example 1</span></span>
```powershell
PS C:\> New-AzNetAppFilesBackup -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyVolumeBackup" -Label "ALabel"
```

<span data-ttu-id="13b78-111">Эта команда создает новую резервную копию ANF для тома с именем учетной записи "MyVolume".</span><span class="sxs-lookup"><span data-stu-id="13b78-111">This command creates the new ANF backup for volume named  account "MyVolume".</span></span>

## <span data-ttu-id="13b78-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13b78-112">PARAMETERS</span></span>

### <span data-ttu-id="13b78-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="13b78-113">-AccountName</span></span>
<span data-ttu-id="13b78-114">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="13b78-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="13b78-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13b78-115">-DefaultProfile</span></span>
<span data-ttu-id="13b78-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="13b78-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13b78-117">-Label</span><span class="sxs-lookup"><span data-stu-id="13b78-117">-Label</span></span>
<span data-ttu-id="13b78-118">Метка для резервного копирования</span><span class="sxs-lookup"><span data-stu-id="13b78-118">Label for backup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13b78-119">-Location</span><span class="sxs-lookup"><span data-stu-id="13b78-119">-Location</span></span>
<span data-ttu-id="13b78-120">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="13b78-120">The location of the resource</span></span>

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

### <span data-ttu-id="13b78-121">-Name</span><span class="sxs-lookup"><span data-stu-id="13b78-121">-Name</span></span>
<span data-ttu-id="13b78-122">Имя резервной копии ANF</span><span class="sxs-lookup"><span data-stu-id="13b78-122">The name of the ANF backup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13b78-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="13b78-123">-PoolName</span></span>
<span data-ttu-id="13b78-124">Имя пула ANF</span><span class="sxs-lookup"><span data-stu-id="13b78-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="13b78-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13b78-125">-ResourceGroupName</span></span>
<span data-ttu-id="13b78-126">Группа ресурсов учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="13b78-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="13b78-127">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="13b78-127">-VolumeName</span></span>
<span data-ttu-id="13b78-128">Название тома ANF</span><span class="sxs-lookup"><span data-stu-id="13b78-128">The name of the ANF volume</span></span>

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

### <span data-ttu-id="13b78-129">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="13b78-129">-VolumeObject</span></span>
<span data-ttu-id="13b78-130">Громкость нового объекта резервной копии</span><span class="sxs-lookup"><span data-stu-id="13b78-130">The volume for the new backup object</span></span>

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

### <span data-ttu-id="13b78-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13b78-131">-Confirm</span></span>
<span data-ttu-id="13b78-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="13b78-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13b78-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13b78-133">-WhatIf</span></span>
<span data-ttu-id="13b78-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13b78-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13b78-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="13b78-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13b78-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13b78-136">CommonParameters</span></span>
<span data-ttu-id="13b78-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13b78-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13b78-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13b78-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13b78-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="13b78-139">INPUTS</span></span>

### <span data-ttu-id="13b78-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="13b78-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="13b78-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="13b78-141">OUTPUTS</span></span>

### <span data-ttu-id="13b78-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="13b78-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="13b78-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="13b78-143">NOTES</span></span>

## <span data-ttu-id="13b78-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="13b78-144">RELATED LINKS</span></span>
