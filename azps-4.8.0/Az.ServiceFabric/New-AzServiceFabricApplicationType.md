---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
ms.openlocfilehash: 690b00c41aea571786916d2055eb4063c51c4370
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243308"
---
# <span data-ttu-id="dd392-101">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="dd392-101">New-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="dd392-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dd392-102">SYNOPSIS</span></span>
<span data-ttu-id="dd392-103">Создание нового типа приложения "структура службы" в заданной группе ресурсов и кластере.</span><span class="sxs-lookup"><span data-stu-id="dd392-103">Create new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="dd392-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dd392-104">SYNTAX</span></span>

```
New-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd392-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd392-105">DESCRIPTION</span></span>
<span data-ttu-id="dd392-106">Командлет создает новый тип приложения фабрики служб в заданной группе ресурсов и кластере.</span><span class="sxs-lookup"><span data-stu-id="dd392-106">The cmdlet creates a new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="dd392-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dd392-107">EXAMPLES</span></span>

### <span data-ttu-id="dd392-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dd392-108">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appType = New-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="dd392-109">В этом примере создается новый тип приложения "testAppType" в группе ресурсов и в указанном кластере.</span><span class="sxs-lookup"><span data-stu-id="dd392-109">This example will create a new application type "testAppType" under the resource group and cluster specified.</span></span>

## <span data-ttu-id="dd392-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dd392-110">PARAMETERS</span></span>

### <span data-ttu-id="dd392-111">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="dd392-111">-ClusterName</span></span>
<span data-ttu-id="dd392-112">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="dd392-112">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd392-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd392-113">-DefaultProfile</span></span>
<span data-ttu-id="dd392-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dd392-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd392-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dd392-115">-Name</span></span>
<span data-ttu-id="dd392-116">Укажите имя типа приложения.</span><span class="sxs-lookup"><span data-stu-id="dd392-116">Specify the name of the application type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd392-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd392-117">-ResourceGroupName</span></span>
<span data-ttu-id="dd392-118">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dd392-118">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd392-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd392-119">-Confirm</span></span>
<span data-ttu-id="dd392-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dd392-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd392-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd392-121">-WhatIf</span></span>
<span data-ttu-id="dd392-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dd392-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd392-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dd392-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd392-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd392-124">CommonParameters</span></span>
<span data-ttu-id="dd392-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dd392-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd392-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd392-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd392-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dd392-127">INPUTS</span></span>

### <span data-ttu-id="dd392-128">System. String</span><span class="sxs-lookup"><span data-stu-id="dd392-128">System.String</span></span>

## <span data-ttu-id="dd392-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd392-129">OUTPUTS</span></span>

### <span data-ttu-id="dd392-130">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="dd392-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="dd392-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="dd392-131">NOTES</span></span>

## <span data-ttu-id="dd392-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dd392-132">RELATED LINKS</span></span>
