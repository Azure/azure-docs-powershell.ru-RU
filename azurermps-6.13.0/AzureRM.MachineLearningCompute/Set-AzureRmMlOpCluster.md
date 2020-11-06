---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/set-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Set-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Set-AzureRmMlOpCluster.md
ms.openlocfilehash: cbe72d14eac4864b784f31c4a800db09fc38b042
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564339"
---
# <span data-ttu-id="74f79-101">Set-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="74f79-101">Set-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="74f79-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="74f79-102">SYNOPSIS</span></span>
<span data-ttu-id="74f79-103">Задает свойства кластера операций.</span><span class="sxs-lookup"><span data-stu-id="74f79-103">Sets the properties of an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74f79-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="74f79-104">SYNTAX</span></span>

### <span data-ttu-id="74f79-105">SetByIndividualParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="74f79-105">SetByIndividualParameters (Default)</span></span>
```
Set-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74f79-106">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="74f79-106">SetByInputObject</span></span>
```
Set-AzureRmMlOpCluster -InputObject <PSOperationalizationCluster> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74f79-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="74f79-107">SetByResourceId</span></span>
```
Set-AzureRmMlOpCluster -ResourceId <String> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74f79-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="74f79-108">DESCRIPTION</span></span>
<span data-ttu-id="74f79-109">Задает все свойства кластера операций.</span><span class="sxs-lookup"><span data-stu-id="74f79-109">Sets all the properties of an operationalization cluster.</span></span> <span data-ttu-id="74f79-110">Так как при использовании объекта кластера устанавливаются все свойства, необходимо передать полный допустимый объект ввода.</span><span class="sxs-lookup"><span data-stu-id="74f79-110">Since it sets all the properties when using a cluster object a fully valid input object must be passed.</span></span> <span data-ttu-id="74f79-111">Свойства, предназначенные только для чтения, будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="74f79-111">Read-only properties will be ignored.</span></span> <span data-ttu-id="74f79-112">В настоящее время поддерживается обновление только некоторых свойств, как показано в наборах параметров.</span><span class="sxs-lookup"><span data-stu-id="74f79-112">Only some properties are currently updatable, as shown in the parameter sets.</span></span>

## <span data-ttu-id="74f79-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="74f79-113">EXAMPLES</span></span>

### <span data-ttu-id="74f79-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="74f79-114">Example 1</span></span>
<span data-ttu-id="74f79-115">Обновление кластера с использованием отдельных параметров.</span><span class="sxs-lookup"><span data-stu-id="74f79-115">Update a cluster using individual parameters.</span></span>

```
PS C:\> Set-AzureRmMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster -AgentCount 5
```

### <span data-ttu-id="74f79-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="74f79-116">Example 2</span></span>
<span data-ttu-id="74f79-117">Обновите кластер с помощью объекта ввода.</span><span class="sxs-lookup"><span data-stu-id="74f79-117">Update a cluster using an input object.</span></span>

```
PS C:\> $cluster = Get-AzureRmMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster
PS C:\> $cluster.ContainerService.AgentCount = 5
PS C:\> Set-AzureRmMlOpCluster -InputObject $cluster
```

## <span data-ttu-id="74f79-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="74f79-118">PARAMETERS</span></span>

### <span data-ttu-id="74f79-119">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="74f79-119">-AgentCount</span></span>
<span data-ttu-id="74f79-120">Количество узлов агента в кластере ACS.</span><span class="sxs-lookup"><span data-stu-id="74f79-120">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74f79-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74f79-121">-DefaultProfile</span></span>
<span data-ttu-id="74f79-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="74f79-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74f79-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74f79-123">-InputObject</span></span>
<span data-ttu-id="74f79-124">Свойства кластера для операционной работы.</span><span class="sxs-lookup"><span data-stu-id="74f79-124">The operationalization cluster properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: SetByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74f79-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="74f79-125">-Name</span></span>
<span data-ttu-id="74f79-126">Название кластера операций.</span><span class="sxs-lookup"><span data-stu-id="74f79-126">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74f79-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74f79-127">-ResourceGroupName</span></span>
<span data-ttu-id="74f79-128">Имя группы ресурсов для кластера операций.</span><span class="sxs-lookup"><span data-stu-id="74f79-128">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74f79-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74f79-129">-ResourceId</span></span>
<span data-ttu-id="74f79-130">Идентификатор ресурса Azure для кластера "эксплуатация".</span><span class="sxs-lookup"><span data-stu-id="74f79-130">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74f79-131">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="74f79-131">-SslCertificate</span></span>
<span data-ttu-id="74f79-132">Данные сертификата SSL в формате PEM.</span><span class="sxs-lookup"><span data-stu-id="74f79-132">The SSL certificate data in PEM format.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74f79-133">-SslCName</span><span class="sxs-lookup"><span data-stu-id="74f79-133">-SslCName</span></span>
<span data-ttu-id="74f79-134">CName-запись сертификата SSL.</span><span class="sxs-lookup"><span data-stu-id="74f79-134">The CName for the SSL certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74f79-135">-SslKey</span><span class="sxs-lookup"><span data-stu-id="74f79-135">-SslKey</span></span>
<span data-ttu-id="74f79-136">Данные ключа SSL в формате PEM.</span><span class="sxs-lookup"><span data-stu-id="74f79-136">The SSL key data in PEM format.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74f79-137">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="74f79-137">-SslStatus</span></span>
<span data-ttu-id="74f79-138">Состояние SSL.</span><span class="sxs-lookup"><span data-stu-id="74f79-138">SSL status.</span></span>
<span data-ttu-id="74f79-139">Возможны значения "включено" и "отключено".</span><span class="sxs-lookup"><span data-stu-id="74f79-139">Possible values are 'Enabled' and 'Disabled'.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74f79-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="74f79-140">-Confirm</span></span>
<span data-ttu-id="74f79-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="74f79-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74f79-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74f79-142">-WhatIf</span></span>
<span data-ttu-id="74f79-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="74f79-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74f79-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="74f79-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74f79-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74f79-145">CommonParameters</span></span>
<span data-ttu-id="74f79-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="74f79-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74f79-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74f79-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74f79-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="74f79-148">INPUTS</span></span>

### <span data-ttu-id="74f79-149">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="74f79-149">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="74f79-150">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="74f79-150">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="74f79-151">System. String</span><span class="sxs-lookup"><span data-stu-id="74f79-151">System.String</span></span>

### <span data-ttu-id="74f79-152">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="74f79-152">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="74f79-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="74f79-153">OUTPUTS</span></span>

### <span data-ttu-id="74f79-154">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="74f79-154">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="74f79-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="74f79-155">NOTES</span></span>

## <span data-ttu-id="74f79-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="74f79-156">RELATED LINKS</span></span>
