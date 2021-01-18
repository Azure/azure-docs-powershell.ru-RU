---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVolume.md
ms.openlocfilehash: 1a04f128326c0b2259b81d6c58c4bc7b0113e9db
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505019"
---
# <span data-ttu-id="c8717-101">Get-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="c8717-101">Get-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="c8717-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8717-102">SYNOPSIS</span></span>
<span data-ttu-id="c8717-103">Подробные сведения о том, где есть файлы Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="c8717-103">Gets details of an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="c8717-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c8717-104">SYNTAX</span></span>

### <span data-ttu-id="c8717-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c8717-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8717-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8717-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesVolume -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8717-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8717-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesVolume -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c8717-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8717-108">DESCRIPTION</span></span>
<span data-ttu-id="c8717-109">Для получения подробных сведений о том, как получить anF-том, можно получить подробные сведения о **cmdlet Get-AzNetAppFilesVolume.**</span><span class="sxs-lookup"><span data-stu-id="c8717-109">The **Get-AzNetAppFilesVolume** cmdlet gets details of an ANF volume.</span></span>

## <span data-ttu-id="c8717-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c8717-110">EXAMPLES</span></span>

### <span data-ttu-id="c8717-111">Пример 1. Получить том ANF</span><span class="sxs-lookup"><span data-stu-id="c8717-111">Example 1: Get an ANF volume</span></span>
```
PS C:\>Get-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume"

Output:

ResourceGroupName : MyRG
Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     :
ServiceLevel      : Premium
UsageThreshold    : 1099511627776
ProvisioningState : Succeeded
SubnetId          : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyRG-vnet/subnets/default
```

<span data-ttu-id="c8717-112">Эта команда получает громкость MyAnfVolume из пула "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="c8717-112">This command gets the volume named MyAnfVolume from the pool "MyAnfPool".</span></span> 

## <span data-ttu-id="c8717-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8717-113">PARAMETERS</span></span>

### <span data-ttu-id="c8717-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c8717-114">-AccountName</span></span>
<span data-ttu-id="c8717-115">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="c8717-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="c8717-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8717-116">-DefaultProfile</span></span>
<span data-ttu-id="c8717-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c8717-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8717-118">-Name</span><span class="sxs-lookup"><span data-stu-id="c8717-118">-Name</span></span>
<span data-ttu-id="c8717-119">Название тома ANF</span><span class="sxs-lookup"><span data-stu-id="c8717-119">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8717-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="c8717-120">-PoolName</span></span>
<span data-ttu-id="c8717-121">Имя пула ANF</span><span class="sxs-lookup"><span data-stu-id="c8717-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="c8717-122">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="c8717-122">-PoolObject</span></span>
<span data-ttu-id="c8717-123">Объект пула, содержащий объем, который нужно вернуть</span><span class="sxs-lookup"><span data-stu-id="c8717-123">The pool object containing the volume to return</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8717-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8717-124">-ResourceGroupName</span></span>
<span data-ttu-id="c8717-125">Группа ресурсов для тома ANF</span><span class="sxs-lookup"><span data-stu-id="c8717-125">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="c8717-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c8717-126">-ResourceId</span></span>
<span data-ttu-id="c8717-127">ИД ресурса для тома ANF</span><span class="sxs-lookup"><span data-stu-id="c8717-127">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="c8717-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8717-128">CommonParameters</span></span>
<span data-ttu-id="c8717-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8717-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8717-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8717-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8717-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c8717-131">INPUTS</span></span>

### <span data-ttu-id="c8717-132">System.String</span><span class="sxs-lookup"><span data-stu-id="c8717-132">System.String</span></span>

### <span data-ttu-id="c8717-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="c8717-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="c8717-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c8717-134">OUTPUTS</span></span>

### <span data-ttu-id="c8717-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="c8717-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="c8717-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c8717-136">NOTES</span></span>

## <span data-ttu-id="c8717-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c8717-137">RELATED LINKS</span></span>
