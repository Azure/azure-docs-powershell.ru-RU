---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/set-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Set-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Set-AzureRmMlOpCluster.md
ms.openlocfilehash: 142dd983b00b578f47e2c1f2eebcbd0686614430
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734701"
---
# <span data-ttu-id="01a48-101">Set-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="01a48-101">Set-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="01a48-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="01a48-102">SYNOPSIS</span></span>
<span data-ttu-id="01a48-103">Задает свойства кластера операций.</span><span class="sxs-lookup"><span data-stu-id="01a48-103">Sets the properties of an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01a48-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="01a48-104">SYNTAX</span></span>

### <span data-ttu-id="01a48-105">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="01a48-105">SetByInputObject</span></span>
```
Set-AzureRmMlOpCluster -InputObject <PSOperationalizationCluster> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="01a48-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="01a48-106">SetByResourceId</span></span>
```
Set-AzureRmMlOpCluster -ResourceId <String> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="01a48-107">SetByIndividualParameters</span><span class="sxs-lookup"><span data-stu-id="01a48-107">SetByIndividualParameters</span></span>
```
Set-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="01a48-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="01a48-108">DESCRIPTION</span></span>
<span data-ttu-id="01a48-109">Задает все свойства кластера операций.</span><span class="sxs-lookup"><span data-stu-id="01a48-109">Sets all the properties of an operationalization cluster.</span></span> <span data-ttu-id="01a48-110">Так как при использовании объекта кластера устанавливаются все свойства, необходимо передать полный допустимый объект ввода.</span><span class="sxs-lookup"><span data-stu-id="01a48-110">Since it sets all the properties when using a cluster object a fully valid input object must be passed.</span></span> <span data-ttu-id="01a48-111">Свойства, предназначенные только для чтения, будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="01a48-111">Read-only properties will be ignored.</span></span> <span data-ttu-id="01a48-112">В настоящее время поддерживается обновление только некоторых свойств, как показано в наборах параметров.</span><span class="sxs-lookup"><span data-stu-id="01a48-112">Only some properties are currently updatable, as shown in the parameter sets.</span></span>

## <span data-ttu-id="01a48-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="01a48-113">EXAMPLES</span></span>

### <span data-ttu-id="01a48-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="01a48-114">Example 1</span></span>
<span data-ttu-id="01a48-115">Обновление кластера с использованием отдельных параметров.</span><span class="sxs-lookup"><span data-stu-id="01a48-115">Update a cluster using individual parameters.</span></span>
```
PS C:\> Set-AzureRmMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster -AgentCount 5
```

### <span data-ttu-id="01a48-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="01a48-116">Example 2</span></span>
<span data-ttu-id="01a48-117">Обновите кластер с помощью объекта ввода.</span><span class="sxs-lookup"><span data-stu-id="01a48-117">Update a cluster using an input object.</span></span>
```
PS C:\> $cluster = Get-AzureRmMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster
PS C:\> $cluster.ContainerService.AgentCount = 5
PS C:\> Set-AzureRmMlOpCluster -InputObject $cluster
```

## <span data-ttu-id="01a48-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="01a48-118">PARAMETERS</span></span>

### <span data-ttu-id="01a48-119">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="01a48-119">-AgentCount</span></span>
<span data-ttu-id="01a48-120">Количество узлов агента в кластере ACS.</span><span class="sxs-lookup"><span data-stu-id="01a48-120">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByInputObject, SetByResourceId, SetByIndividualParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01a48-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01a48-121">-DefaultProfile</span></span>
<span data-ttu-id="01a48-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="01a48-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01a48-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01a48-123">-InputObject</span></span>
<span data-ttu-id="01a48-124">Свойства кластера для операционной работы.</span><span class="sxs-lookup"><span data-stu-id="01a48-124">The operationalization cluster properties.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: SetByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01a48-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="01a48-125">-Name</span></span>
<span data-ttu-id="01a48-126">Название кластера операций.</span><span class="sxs-lookup"><span data-stu-id="01a48-126">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: SetByIndividualParameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01a48-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01a48-127">-ResourceGroupName</span></span>
<span data-ttu-id="01a48-128">Имя группы ресурсов для кластера операций.</span><span class="sxs-lookup"><span data-stu-id="01a48-128">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: SetByIndividualParameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01a48-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01a48-129">-ResourceId</span></span>
<span data-ttu-id="01a48-130">Идентификатор ресурса Azure для кластера "эксплуатация".</span><span class="sxs-lookup"><span data-stu-id="01a48-130">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01a48-131">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="01a48-131">-SslCertificate</span></span>
<span data-ttu-id="01a48-132">Данные сертификата SSL в формате PEM.</span><span class="sxs-lookup"><span data-stu-id="01a48-132">The SSL certificate data in PEM format.</span></span>

```yaml
Type: String
Parameter Sets: SetByInputObject, SetByResourceId, SetByIndividualParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01a48-133">-SslCName</span><span class="sxs-lookup"><span data-stu-id="01a48-133">-SslCName</span></span>
<span data-ttu-id="01a48-134">CName-запись сертификата SSL.</span><span class="sxs-lookup"><span data-stu-id="01a48-134">The CName for the SSL certificate.</span></span>

```yaml
Type: String
Parameter Sets: SetByInputObject, SetByResourceId, SetByIndividualParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01a48-135">-SslKey</span><span class="sxs-lookup"><span data-stu-id="01a48-135">-SslKey</span></span>
<span data-ttu-id="01a48-136">Данные ключа SSL в формате PEM.</span><span class="sxs-lookup"><span data-stu-id="01a48-136">The SSL key data in PEM format.</span></span>

```yaml
Type: String
Parameter Sets: SetByInputObject, SetByResourceId, SetByIndividualParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01a48-137">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="01a48-137">-SslStatus</span></span>
<span data-ttu-id="01a48-138">Состояние SSL.</span><span class="sxs-lookup"><span data-stu-id="01a48-138">SSL status.</span></span>
<span data-ttu-id="01a48-139">Возможны значения "включено" и "отключено".</span><span class="sxs-lookup"><span data-stu-id="01a48-139">Possible values are 'Enabled' and 'Disabled'.</span></span>

```yaml
Type: String
Parameter Sets: SetByInputObject, SetByResourceId, SetByIndividualParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01a48-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01a48-140">-Confirm</span></span>
<span data-ttu-id="01a48-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="01a48-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01a48-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01a48-142">-WhatIf</span></span>
<span data-ttu-id="01a48-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="01a48-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01a48-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="01a48-144">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="01a48-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="01a48-145">INPUTS</span></span>

### <span data-ttu-id="01a48-146">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="01a48-146">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
### <span data-ttu-id="01a48-147">System. String</span><span class="sxs-lookup"><span data-stu-id="01a48-147">System.String</span></span>
### <span data-ttu-id="01a48-148">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="01a48-148">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>


## <span data-ttu-id="01a48-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="01a48-149">OUTPUTS</span></span>

### <span data-ttu-id="01a48-150">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="01a48-150">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>


## <span data-ttu-id="01a48-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="01a48-151">NOTES</span></span>

## <span data-ttu-id="01a48-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="01a48-152">RELATED LINKS</span></span>

