---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationService.md
ms.openlocfilehash: c8e81cf727894adfa7378bbed996a1a476521148
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313118"
---
# <span data-ttu-id="a2749-101">New-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="a2749-101">New-AzDataMigrationService</span></span>

## <span data-ttu-id="a2749-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a2749-102">SYNOPSIS</span></span>
<span data-ttu-id="a2749-103">Создание нового экземпляра службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="a2749-103">Creates a new instance of the Azure Database Migration Service.</span></span>

## <span data-ttu-id="a2749-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a2749-104">SYNTAX</span></span>

```
New-AzDataMigrationService -ResourceGroupName <String> -Name <String> -Location <String> -Sku <String>
 -VirtualSubnetId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2749-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2749-105">DESCRIPTION</span></span>
<span data-ttu-id="a2749-106">Командлет New-AzDataMigrationService создает новый экземпляр службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="a2749-106">The New-AzDataMigrationService cmdlet creates a new instance of the Azure Database Migration Service.</span></span> <span data-ttu-id="a2749-107">Этот командлет принимает имя существующей группы ресурсов Azure, уникальное имя для нового экземпляра службы миграции баз данных Azure, область, в которой выполняется подготовка экземпляра, имя SKU рабочего процесса DMS и имя виртуальной подсети Azure, в которой будет находиться служба.</span><span class="sxs-lookup"><span data-stu-id="a2749-107">This cmdlet takes in name of existing Azure Resource Group, the unique name for the new instance of the Azure Database Migration Service to be created, the region in which the instance is provisioned, the name of the DMS Worker SKU, and the name of the Azure Virtual Subnet on which the service is to reside.</span></span> <span data-ttu-id="a2749-108">Для имени подписки нет параметра, так как ожидается, что пользователь должен указать подписку по умолчанию для сеанса входа Azure или выполнить Get-AzSubscription-SubscriptionName "MySubscription" | Select-AzSubscription, чтобы выбрать другую подписку.</span><span class="sxs-lookup"><span data-stu-id="a2749-108">There is no parameter for subscription name, because it is expected for the user to specify the default subscription of the Azure login session or execute Get-AzSubscription -SubscriptionName "MySubscription" | Select-AzSubscription to select another subscription.</span></span>

## <span data-ttu-id="a2749-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a2749-109">EXAMPLES</span></span>

### <span data-ttu-id="a2749-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a2749-110">Example 1</span></span>
```
PS C:\> New-AzDataMigrationService -ResourceGroupName myResourceGroup -Name TestService -Location "Central US" -Sku Basic_2vCores -VirtualSubnetId $virtualSubNetId
```

<span data-ttu-id="a2749-111">В приведенном выше примере показано, как создать новый экземпляр службы миграции баз данных Azure с именем TestService в центральном регионе США.</span><span class="sxs-lookup"><span data-stu-id="a2749-111">The above example shows how to create a new instance of the Azure Database Migration Service named TestService in Central US region.</span></span>

## <span data-ttu-id="a2749-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a2749-112">PARAMETERS</span></span>

### <span data-ttu-id="a2749-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2749-113">-DefaultProfile</span></span>
<span data-ttu-id="a2749-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a2749-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2749-115">-Location</span><span class="sxs-lookup"><span data-stu-id="a2749-115">-Location</span></span>
<span data-ttu-id="a2749-116">Расположение создаваемого экземпляра службы миграции баз данных Azure, которое соответствует региону Azure.</span><span class="sxs-lookup"><span data-stu-id="a2749-116">The location of the Azure Database Migration Service instance to be created, which corresponds to an Azure region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2749-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a2749-117">-Name</span></span>
<span data-ttu-id="a2749-118">Имя службы миграции баз данных.</span><span class="sxs-lookup"><span data-stu-id="a2749-118">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2749-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2749-119">-ResourceGroupName</span></span>
<span data-ttu-id="a2749-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a2749-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2749-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="a2749-121">-Sku</span></span>
<span data-ttu-id="a2749-122">SKU для экземпляра службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="a2749-122">The sku for the Azure Database Migration Service instance.</span></span> <span data-ttu-id="a2749-123">В настоящее время доступны значения Basic_1vCore, Basic_2vCores GeneralPurpose_4vCores</span><span class="sxs-lookup"><span data-stu-id="a2749-123">Possible values currently are Basic_1vCore,Basic_2vCores,GeneralPurpose_4vCores</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2749-124">-VirtualSubnetId</span><span class="sxs-lookup"><span data-stu-id="a2749-124">-VirtualSubnetId</span></span>
<span data-ttu-id="a2749-125">Имя подсети в указанной виртуальной сети, используемой для экземпляра службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="a2749-125">The name of the subnet under the specified virtual network to use for the Azure Database Migration Service instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2749-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2749-126">-Confirm</span></span>
<span data-ttu-id="a2749-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a2749-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2749-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2749-128">-WhatIf</span></span>
<span data-ttu-id="a2749-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a2749-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a2749-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a2749-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2749-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2749-131">CommonParameters</span></span>
<span data-ttu-id="a2749-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a2749-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2749-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2749-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2749-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a2749-134">INPUTS</span></span>

### <span data-ttu-id="a2749-135">Ничего</span><span class="sxs-lookup"><span data-stu-id="a2749-135">None</span></span>

## <span data-ttu-id="a2749-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2749-136">OUTPUTS</span></span>

### <span data-ttu-id="a2749-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="a2749-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="a2749-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="a2749-138">NOTES</span></span>

## <span data-ttu-id="a2749-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a2749-139">RELATED LINKS</span></span>
