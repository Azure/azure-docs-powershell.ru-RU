---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8CD55A33-5964-409A-BDA5-EDAE9A21E0C1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: 91e5a0fbb92ced1c79717aecb01d5896bb422280
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94080004"
---
# <span data-ttu-id="2c6ea-101">Get-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c6ea-101">Get-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="2c6ea-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2c6ea-102">SYNOPSIS</span></span>
<span data-ttu-id="2c6ea-103">Получает конфигурацию автомасштабирования кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2c6ea-103">Gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="2c6ea-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2c6ea-104">SYNTAX</span></span>

### <span data-ttu-id="2c6ea-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2c6ea-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c6ea-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c6ea-106">GetByResourceIdParameterSet</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2c6ea-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c6ea-107">GetByInputObjectParameterSet</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c6ea-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c6ea-108">DESCRIPTION</span></span>
<span data-ttu-id="2c6ea-109">Командлет **Get-AzHDInsightClusterAutoscaleConfiguration** получает конфигурацию автомасштабирования кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2c6ea-109">The **Get-AzHDInsightClusterAutoscaleConfiguration** cmdlet gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="2c6ea-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2c6ea-110">EXAMPLES</span></span>

### <span data-ttu-id="2c6ea-111">Пример 1: получение конфигурации автомасштабирования в кластере HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2c6ea-111">Example 1: Get the autoscale configuration of HDInsight cluster.</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Get-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName
```

<span data-ttu-id="2c6ea-112">Эта команда получает конфигурацию автоматического масштабирования кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2c6ea-112">This command gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="2c6ea-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2c6ea-113">PARAMETERS</span></span>

### <span data-ttu-id="2c6ea-114">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="2c6ea-114">-ClusterName</span></span>
<span data-ttu-id="2c6ea-115">Возвращает или задает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="2c6ea-115">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="2c6ea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c6ea-116">-DefaultProfile</span></span>
<span data-ttu-id="2c6ea-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2c6ea-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c6ea-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c6ea-118">-InputObject</span></span>
<span data-ttu-id="2c6ea-119">Возвращает или задает объект ввода.</span><span class="sxs-lookup"><span data-stu-id="2c6ea-119">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="2c6ea-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c6ea-120">-ResourceGroupName</span></span>
<span data-ttu-id="2c6ea-121">Возвращает или задает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2c6ea-121">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="2c6ea-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c6ea-122">-ResourceId</span></span>
<span data-ttu-id="2c6ea-123">Возвращает или задает идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="2c6ea-123">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="2c6ea-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c6ea-124">CommonParameters</span></span>
<span data-ttu-id="2c6ea-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2c6ea-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c6ea-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c6ea-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c6ea-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2c6ea-127">INPUTS</span></span>

### <span data-ttu-id="2c6ea-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2c6ea-128">System.String</span></span>

### <span data-ttu-id="2c6ea-129">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="2c6ea-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="2c6ea-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c6ea-130">OUTPUTS</span></span>

### <span data-ttu-id="2c6ea-131">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightAutoscale</span><span class="sxs-lookup"><span data-stu-id="2c6ea-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="2c6ea-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="2c6ea-132">NOTES</span></span>

## <span data-ttu-id="2c6ea-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2c6ea-133">RELATED LINKS</span></span>

<span data-ttu-id="2c6ea-134">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2c6ea-134">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
