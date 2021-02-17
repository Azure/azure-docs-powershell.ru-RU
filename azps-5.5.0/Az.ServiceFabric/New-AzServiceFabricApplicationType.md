---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
ms.openlocfilehash: 690b00c41aea571786916d2055eb4063c51c4370
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232724"
---
# <span data-ttu-id="ba598-101">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ba598-101">New-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="ba598-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba598-102">SYNOPSIS</span></span>
<span data-ttu-id="ba598-103">Создайте новый тип приложения-службы в указанной группе ресурсов и кластере.</span><span class="sxs-lookup"><span data-stu-id="ba598-103">Create new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="ba598-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ba598-104">SYNTAX</span></span>

```
New-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba598-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba598-105">DESCRIPTION</span></span>
<span data-ttu-id="ba598-106">С его рабочая группа создается новый тип приложения-услуги в указанной группе ресурсов и кластере.</span><span class="sxs-lookup"><span data-stu-id="ba598-106">The cmdlet creates a new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="ba598-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ba598-107">EXAMPLES</span></span>

### <span data-ttu-id="ba598-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ba598-108">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appType = New-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="ba598-109">В этом примере создается новый тип приложения TestAppType под указанной группой ресурсов и кластером ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ba598-109">This example will create a new application type "testAppType" under the resource group and cluster specified.</span></span>

## <span data-ttu-id="ba598-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba598-110">PARAMETERS</span></span>

### <span data-ttu-id="ba598-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ba598-111">-ClusterName</span></span>
<span data-ttu-id="ba598-112">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="ba598-112">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="ba598-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba598-113">-DefaultProfile</span></span>
<span data-ttu-id="ba598-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ba598-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba598-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ba598-115">-Name</span></span>
<span data-ttu-id="ba598-116">Указание имени типа приложения</span><span class="sxs-lookup"><span data-stu-id="ba598-116">Specify the name of the application type</span></span>

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

### <span data-ttu-id="ba598-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba598-117">-ResourceGroupName</span></span>
<span data-ttu-id="ba598-118">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ba598-118">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="ba598-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba598-119">-Confirm</span></span>
<span data-ttu-id="ba598-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba598-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba598-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba598-121">-WhatIf</span></span>
<span data-ttu-id="ba598-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba598-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba598-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ba598-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba598-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba598-124">CommonParameters</span></span>
<span data-ttu-id="ba598-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba598-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba598-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ba598-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba598-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ba598-127">INPUTS</span></span>

### <span data-ttu-id="ba598-128">System.String</span><span class="sxs-lookup"><span data-stu-id="ba598-128">System.String</span></span>

## <span data-ttu-id="ba598-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ba598-129">OUTPUTS</span></span>

### <span data-ttu-id="ba598-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="ba598-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="ba598-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ba598-131">NOTES</span></span>

## <span data-ttu-id="ba598-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ba598-132">RELATED LINKS</span></span>
