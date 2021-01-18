---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 0f1b6806565a21b106816019c08641e269c4d5a8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505024"
---
# <span data-ttu-id="6c99e-101">Get-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="6c99e-101">Get-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="6c99e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c99e-102">SYNOPSIS</span></span>
<span data-ttu-id="6c99e-103">Сведения о моментальных снимках файлов в Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="6c99e-103">Gets details of an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="6c99e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6c99e-104">SYNTAX</span></span>

### <span data-ttu-id="6c99e-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6c99e-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c99e-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c99e-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesSnapshot [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6c99e-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c99e-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesSnapshot [-Name <String>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c99e-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c99e-108">DESCRIPTION</span></span>
<span data-ttu-id="6c99e-109">Для получения подробных сведений о снимке ANF возвращается **cmdlet Get-AzNetAppFilesSnapshot.**</span><span class="sxs-lookup"><span data-stu-id="6c99e-109">The **Get-AzNetAppFilesSnapshot** cmdlet gets details of an ANF snapshot.</span></span>

## <span data-ttu-id="6c99e-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6c99e-110">EXAMPLES</span></span>

### <span data-ttu-id="6c99e-111">Пример 1. Получить снимок ANF</span><span class="sxs-lookup"><span data-stu-id="6c99e-111">Example 1: Get an ANF snapshot</span></span>
```
PS C:\>Get-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -Name "MyAnfSnapshot"

Output:

ResourceGroupName : MyRG
Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume/snapshots/MyAnfSnapshot
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume/MyAnfSnapshot
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes/snapshots
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
SnapshotId        : ca7c4ebd-91cb-0e30-91f5-9154050033df
Created           :
ProvisioningState : Succeeded
```

<span data-ttu-id="6c99e-112">Эта команда получает снимок с именем MyAnfSnapshot из тома "MyAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="6c99e-112">This command gets the snapshot named MyAnfSnapshot from the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="6c99e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c99e-113">PARAMETERS</span></span>

### <span data-ttu-id="6c99e-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6c99e-114">-AccountName</span></span>
<span data-ttu-id="6c99e-115">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="6c99e-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="6c99e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c99e-116">-DefaultProfile</span></span>
<span data-ttu-id="6c99e-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6c99e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c99e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="6c99e-118">-Name</span></span>
<span data-ttu-id="6c99e-119">Имя моментального снимка ANF</span><span class="sxs-lookup"><span data-stu-id="6c99e-119">The name of the ANF snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SnapshotName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c99e-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="6c99e-120">-PoolName</span></span>
<span data-ttu-id="6c99e-121">Имя пула ANF</span><span class="sxs-lookup"><span data-stu-id="6c99e-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="6c99e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c99e-122">-ResourceGroupName</span></span>
<span data-ttu-id="6c99e-123">Группа ресурсов тома ANF</span><span class="sxs-lookup"><span data-stu-id="6c99e-123">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="6c99e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c99e-124">-ResourceId</span></span>
<span data-ttu-id="6c99e-125">The resource id of the ANF snapshot</span><span class="sxs-lookup"><span data-stu-id="6c99e-125">The resource id of the ANF snapshot</span></span>

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

### <span data-ttu-id="6c99e-126">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="6c99e-126">-VolumeName</span></span>
<span data-ttu-id="6c99e-127">Название тома ANF</span><span class="sxs-lookup"><span data-stu-id="6c99e-127">The name of the ANF volume</span></span>

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

### <span data-ttu-id="6c99e-128">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="6c99e-128">-VolumeObject</span></span>
<span data-ttu-id="6c99e-129">Объект громкости, содержащий моментальный снимок, который нужно вернуть</span><span class="sxs-lookup"><span data-stu-id="6c99e-129">The volume object containing the snapshot to return</span></span>

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

### <span data-ttu-id="6c99e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c99e-130">CommonParameters</span></span>
<span data-ttu-id="6c99e-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c99e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c99e-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6c99e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c99e-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6c99e-133">INPUTS</span></span>

### <span data-ttu-id="6c99e-134">System.String</span><span class="sxs-lookup"><span data-stu-id="6c99e-134">System.String</span></span>

### <span data-ttu-id="6c99e-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="6c99e-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="6c99e-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6c99e-136">OUTPUTS</span></span>

### <span data-ttu-id="6c99e-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="6c99e-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="6c99e-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6c99e-138">NOTES</span></span>

## <span data-ttu-id="6c99e-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6c99e-139">RELATED LINKS</span></span>
