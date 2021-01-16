---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackup.md
ms.openlocfilehash: 46f6f5d7f9d843a9dd6d30053e9205e52be989d4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410831"
---
# <span data-ttu-id="201f2-101">Get-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="201f2-101">Get-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="201f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="201f2-102">SYNOPSIS</span></span>
<span data-ttu-id="201f2-103">Сведения о резервной копии Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="201f2-103">Gets details of an Azure NetApp Files (ANF) Backup.</span></span>

## <span data-ttu-id="201f2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="201f2-104">SYNTAX</span></span>

### <span data-ttu-id="201f2-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="201f2-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesBackup -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 [-VolumeName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="201f2-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="201f2-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesBackup [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="201f2-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="201f2-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesBackup [-Name <String>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="201f2-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="201f2-108">DESCRIPTION</span></span>
<span data-ttu-id="201f2-109">Для **получения сведений о резервной копии ANF возвращается cmdlet Get-AzNetAppFilesBackup.**</span><span class="sxs-lookup"><span data-stu-id="201f2-109">The **Get-AzNetAppFilesBackup** cmdlet gets details of an ANF backup.</span></span>

## <span data-ttu-id="201f2-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="201f2-110">EXAMPLES</span></span>

### <span data-ttu-id="201f2-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="201f2-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesBackup -ResourceGroupName "MyRG" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyBackup"
```

<span data-ttu-id="201f2-112">Эта команда возвращает обратное решение с именем MyAnfAccount из тома "MyVolume".</span><span class="sxs-lookup"><span data-stu-id="201f2-112">This command gets the backcup named "MyAnfAccount" from the volume named "MyVolume".</span></span>

## <span data-ttu-id="201f2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="201f2-113">PARAMETERS</span></span>

### <span data-ttu-id="201f2-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="201f2-114">-AccountName</span></span>
<span data-ttu-id="201f2-115">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="201f2-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="201f2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="201f2-116">-DefaultProfile</span></span>
<span data-ttu-id="201f2-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="201f2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="201f2-118">-Name</span><span class="sxs-lookup"><span data-stu-id="201f2-118">-Name</span></span>
<span data-ttu-id="201f2-119">Имя резервной копии ANF</span><span class="sxs-lookup"><span data-stu-id="201f2-119">The name of the ANF backup</span></span>

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

### <span data-ttu-id="201f2-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="201f2-120">-PoolName</span></span>
<span data-ttu-id="201f2-121">Имя пула ANF</span><span class="sxs-lookup"><span data-stu-id="201f2-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="201f2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="201f2-122">-ResourceGroupName</span></span>
<span data-ttu-id="201f2-123">Группа ресурсов учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="201f2-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="201f2-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="201f2-124">-ResourceId</span></span>
<span data-ttu-id="201f2-125">Код ресурса резервной копии ANF</span><span class="sxs-lookup"><span data-stu-id="201f2-125">The resource id of the ANF Backup</span></span>

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

### <span data-ttu-id="201f2-126">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="201f2-126">-VolumeName</span></span>
<span data-ttu-id="201f2-127">Название тома ANF</span><span class="sxs-lookup"><span data-stu-id="201f2-127">The name of the ANF volume</span></span>

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

### <span data-ttu-id="201f2-128">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="201f2-128">-VolumeObject</span></span>
<span data-ttu-id="201f2-129">Объект тома, содержащий резервную копию, возвращаемую</span><span class="sxs-lookup"><span data-stu-id="201f2-129">The volume object containing the backup to return</span></span>

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

### <span data-ttu-id="201f2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="201f2-130">CommonParameters</span></span>
<span data-ttu-id="201f2-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="201f2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="201f2-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="201f2-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="201f2-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="201f2-133">INPUTS</span></span>

### <span data-ttu-id="201f2-134">System.String</span><span class="sxs-lookup"><span data-stu-id="201f2-134">System.String</span></span>

### <span data-ttu-id="201f2-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="201f2-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="201f2-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="201f2-136">OUTPUTS</span></span>

### <span data-ttu-id="201f2-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="201f2-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="201f2-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="201f2-138">NOTES</span></span>

## <span data-ttu-id="201f2-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="201f2-139">RELATED LINKS</span></span>
