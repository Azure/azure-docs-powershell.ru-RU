---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackup.md
ms.openlocfilehash: 46f6f5d7f9d843a9dd6d30053e9205e52be989d4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505029"
---
# <span data-ttu-id="0e7a0-101">Get-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="0e7a0-101">Get-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="0e7a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e7a0-102">SYNOPSIS</span></span>
<span data-ttu-id="0e7a0-103">Сведения о резервной копии Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="0e7a0-103">Gets details of an Azure NetApp Files (ANF) Backup.</span></span>

## <span data-ttu-id="0e7a0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0e7a0-104">SYNTAX</span></span>

### <span data-ttu-id="0e7a0-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0e7a0-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesBackup -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 [-VolumeName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e7a0-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e7a0-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesBackup [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0e7a0-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e7a0-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesBackup [-Name <String>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e7a0-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e7a0-108">DESCRIPTION</span></span>
<span data-ttu-id="0e7a0-109">Для **получения сведений о резервной копии ANF возвращается cmdlet Get-AzNetAppFilesBackup.**</span><span class="sxs-lookup"><span data-stu-id="0e7a0-109">The **Get-AzNetAppFilesBackup** cmdlet gets details of an ANF backup.</span></span>

## <span data-ttu-id="0e7a0-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0e7a0-110">EXAMPLES</span></span>

### <span data-ttu-id="0e7a0-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0e7a0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesBackup -ResourceGroupName "MyRG" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyBackup"
```

<span data-ttu-id="0e7a0-112">Эта команда возвращает обратное решение с именем MyAnfAccount из тома "MyVolume".</span><span class="sxs-lookup"><span data-stu-id="0e7a0-112">This command gets the backcup named "MyAnfAccount" from the volume named "MyVolume".</span></span>

## <span data-ttu-id="0e7a0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e7a0-113">PARAMETERS</span></span>

### <span data-ttu-id="0e7a0-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0e7a0-114">-AccountName</span></span>
<span data-ttu-id="0e7a0-115">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="0e7a0-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="0e7a0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e7a0-116">-DefaultProfile</span></span>
<span data-ttu-id="0e7a0-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0e7a0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e7a0-118">-Name</span><span class="sxs-lookup"><span data-stu-id="0e7a0-118">-Name</span></span>
<span data-ttu-id="0e7a0-119">Имя резервной копии ANF</span><span class="sxs-lookup"><span data-stu-id="0e7a0-119">The name of the ANF backup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e7a0-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="0e7a0-120">-PoolName</span></span>
<span data-ttu-id="0e7a0-121">Имя пула ANF</span><span class="sxs-lookup"><span data-stu-id="0e7a0-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="0e7a0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e7a0-122">-ResourceGroupName</span></span>
<span data-ttu-id="0e7a0-123">Группа ресурсов учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="0e7a0-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="0e7a0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e7a0-124">-ResourceId</span></span>
<span data-ttu-id="0e7a0-125">Код ресурса резервной копии ANF</span><span class="sxs-lookup"><span data-stu-id="0e7a0-125">The resource id of the ANF Backup</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e7a0-126">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="0e7a0-126">-VolumeName</span></span>
<span data-ttu-id="0e7a0-127">Название тома ANF</span><span class="sxs-lookup"><span data-stu-id="0e7a0-127">The name of the ANF volume</span></span>

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

### <span data-ttu-id="0e7a0-128">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="0e7a0-128">-VolumeObject</span></span>
<span data-ttu-id="0e7a0-129">Объект громкости, содержащий резервную копию, возвращаемую</span><span class="sxs-lookup"><span data-stu-id="0e7a0-129">The volume object containing the backup to return</span></span>

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

### <span data-ttu-id="0e7a0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e7a0-130">CommonParameters</span></span>
<span data-ttu-id="0e7a0-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e7a0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e7a0-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e7a0-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e7a0-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0e7a0-133">INPUTS</span></span>

### <span data-ttu-id="0e7a0-134">System.String</span><span class="sxs-lookup"><span data-stu-id="0e7a0-134">System.String</span></span>

### <span data-ttu-id="0e7a0-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="0e7a0-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="0e7a0-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0e7a0-136">OUTPUTS</span></span>

### <span data-ttu-id="0e7a0-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="0e7a0-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="0e7a0-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0e7a0-138">NOTES</span></span>

## <span data-ttu-id="0e7a0-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0e7a0-139">RELATED LINKS</span></span>
