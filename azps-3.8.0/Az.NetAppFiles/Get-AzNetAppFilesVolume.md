---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVolume.md
ms.openlocfilehash: a730bb71ebd6f06bdae4bcbf608987a929a433c3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93911838"
---
# <span data-ttu-id="8cbd1-101">Get-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="8cbd1-101">Get-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="8cbd1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8cbd1-102">SYNOPSIS</span></span>
<span data-ttu-id="8cbd1-103">Получение сведений о томе Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="8cbd1-103">Gets details of an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="8cbd1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8cbd1-104">SYNTAX</span></span>

### <span data-ttu-id="8cbd1-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cbd1-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8cbd1-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesVolume -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cbd1-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8cbd1-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesVolume -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8cbd1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8cbd1-108">DESCRIPTION</span></span>
<span data-ttu-id="8cbd1-109">Командлет **Get-AzNetAppFilesVolume** получает сведения о томе ANF.</span><span class="sxs-lookup"><span data-stu-id="8cbd1-109">The **Get-AzNetAppFilesVolume** cmdlet gets details of an ANF volume.</span></span>

## <span data-ttu-id="8cbd1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8cbd1-110">EXAMPLES</span></span>

### <span data-ttu-id="8cbd1-111">Пример 1: получение ANFого тома</span><span class="sxs-lookup"><span data-stu-id="8cbd1-111">Example 1: Get an ANF volume</span></span>
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

<span data-ttu-id="8cbd1-112">Эта команда получает том с именем MyAnfVolume из пула "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="8cbd1-112">This command gets the volume named MyAnfVolume from the pool "MyAnfPool".</span></span> 

## <span data-ttu-id="8cbd1-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8cbd1-113">PARAMETERS</span></span>

### <span data-ttu-id="8cbd1-114">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="8cbd1-114">-AccountName</span></span>
<span data-ttu-id="8cbd1-115">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="8cbd1-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="8cbd1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cbd1-116">-DefaultProfile</span></span>
<span data-ttu-id="8cbd1-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8cbd1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cbd1-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-118">-Name</span></span>
<span data-ttu-id="8cbd1-119">Имя ANFого тома.</span><span class="sxs-lookup"><span data-stu-id="8cbd1-119">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cbd1-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="8cbd1-120">-PoolName</span></span>
<span data-ttu-id="8cbd1-121">Название пула ANF</span><span class="sxs-lookup"><span data-stu-id="8cbd1-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="8cbd1-122">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="8cbd1-122">-PoolObject</span></span>
<span data-ttu-id="8cbd1-123">Объект пула, содержащий том, который нужно вернуть.</span><span class="sxs-lookup"><span data-stu-id="8cbd1-123">The pool object containing the volume to return</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8cbd1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cbd1-124">-ResourceGroupName</span></span>
<span data-ttu-id="8cbd1-125">Группа ресурсов ANFого тома</span><span class="sxs-lookup"><span data-stu-id="8cbd1-125">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="8cbd1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8cbd1-126">-ResourceId</span></span>
<span data-ttu-id="8cbd1-127">Идентификатор ресурса ANFого тома.</span><span class="sxs-lookup"><span data-stu-id="8cbd1-127">The resource id of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cbd1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cbd1-128">CommonParameters</span></span>
<span data-ttu-id="8cbd1-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8cbd1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="8cbd1-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cbd1-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cbd1-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8cbd1-131">INPUTS</span></span>

### <span data-ttu-id="8cbd1-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8cbd1-132">System.String</span></span>

### <span data-ttu-id="8cbd1-133">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="8cbd1-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="8cbd1-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8cbd1-134">OUTPUTS</span></span>

### <span data-ttu-id="8cbd1-135">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="8cbd1-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="8cbd1-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="8cbd1-136">NOTES</span></span>

## <span data-ttu-id="8cbd1-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8cbd1-137">RELATED LINKS</span></span>
