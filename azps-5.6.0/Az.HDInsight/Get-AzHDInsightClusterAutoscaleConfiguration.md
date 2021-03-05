---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8CD55A33-5964-409A-BDA5-EDAE9A21E0C1
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: 4f60445dc22c2e2b0f8c0c5291691f4d7456db2f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012120"
---
# <span data-ttu-id="4088f-101">Get-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="4088f-101">Get-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="4088f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4088f-102">SYNOPSIS</span></span>
<span data-ttu-id="4088f-103">Получает настройку автоматической настройки кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4088f-103">Gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="4088f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4088f-104">SYNTAX</span></span>

### <span data-ttu-id="4088f-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4088f-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4088f-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4088f-106">GetByResourceIdParameterSet</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4088f-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4088f-107">GetByInputObjectParameterSet</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4088f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4088f-108">DESCRIPTION</span></span>
<span data-ttu-id="4088f-109">Для **работы с кластером HDInsight.cmdlet Get-AzHDInsightClusterAutoscaleConfiguration** получает конфигурацию автомасштабирования кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4088f-109">The **Get-AzHDInsightClusterAutoscaleConfiguration** cmdlet gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="4088f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4088f-110">EXAMPLES</span></span>

### <span data-ttu-id="4088f-111">Пример 1. Настройка автоматической настройки кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4088f-111">Example 1: Get the autoscale configuration of HDInsight cluster.</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Get-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName
```

<span data-ttu-id="4088f-112">Эта команда получает настройку автоматической настройки кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4088f-112">This command gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="4088f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4088f-113">PARAMETERS</span></span>

### <span data-ttu-id="4088f-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4088f-114">-ClusterName</span></span>
<span data-ttu-id="4088f-115">Возвращает или задает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="4088f-115">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4088f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4088f-116">-DefaultProfile</span></span>
<span data-ttu-id="4088f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4088f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4088f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4088f-118">-InputObject</span></span>
<span data-ttu-id="4088f-119">Возвращает или устанавливает объект ввода.</span><span class="sxs-lookup"><span data-stu-id="4088f-119">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4088f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4088f-120">-ResourceGroupName</span></span>
<span data-ttu-id="4088f-121">Возвращает или задает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4088f-121">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4088f-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4088f-122">-ResourceId</span></span>
<span data-ttu-id="4088f-123">Возвращает или задает ид ресурса.</span><span class="sxs-lookup"><span data-stu-id="4088f-123">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4088f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4088f-124">CommonParameters</span></span>
<span data-ttu-id="4088f-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4088f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4088f-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4088f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4088f-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4088f-127">INPUTS</span></span>

### <span data-ttu-id="4088f-128">System.String</span><span class="sxs-lookup"><span data-stu-id="4088f-128">System.String</span></span>

### <span data-ttu-id="4088f-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="4088f-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="4088f-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4088f-130">OUTPUTS</span></span>

### <span data-ttu-id="4088f-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span><span class="sxs-lookup"><span data-stu-id="4088f-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="4088f-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4088f-132">NOTES</span></span>

## <span data-ttu-id="4088f-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4088f-133">RELATED LINKS</span></span>

<span data-ttu-id="4088f-134">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4088f-134">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
