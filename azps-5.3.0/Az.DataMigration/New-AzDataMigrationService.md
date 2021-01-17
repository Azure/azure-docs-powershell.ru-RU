---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationService.md
ms.openlocfilehash: c8e81cf727894adfa7378bbed996a1a476521148
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420868"
---
# <span data-ttu-id="af650-101">New-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="af650-101">New-AzDataMigrationService</span></span>

## <span data-ttu-id="af650-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af650-102">SYNOPSIS</span></span>
<span data-ttu-id="af650-103">Создает новый экземпляр службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="af650-103">Creates a new instance of the Azure Database Migration Service.</span></span>

## <span data-ttu-id="af650-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="af650-104">SYNTAX</span></span>

```
New-AzDataMigrationService -ResourceGroupName <String> -Name <String> -Location <String> -Sku <String>
 -VirtualSubnetId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af650-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="af650-105">DESCRIPTION</span></span>
<span data-ttu-id="af650-106">С New-AzDataMigrationService создается новый экземпляр службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="af650-106">The New-AzDataMigrationService cmdlet creates a new instance of the Azure Database Migration Service.</span></span> <span data-ttu-id="af650-107">Этот cmdlet принимает имя существующей группы ресурсов Azure, уникальное имя нового экземпляра службы миграции баз данных Azure, регион, в котором он предусмотрен, имя SKU "Сотрудник DMS" и имя виртуальной подсети Azure, в которой должна находиться служба.</span><span class="sxs-lookup"><span data-stu-id="af650-107">This cmdlet takes in name of existing Azure Resource Group, the unique name for the new instance of the Azure Database Migration Service to be created, the region in which the instance is provisioned, the name of the DMS Worker SKU, and the name of the Azure Virtual Subnet on which the service is to reside.</span></span> <span data-ttu-id="af650-108">Параметр для имени подписки не задан, так как предполагается, что пользователь указывает стандартную подписку на сеанс входа Azure или выполняет Get-AzSubscription -SubscriptionName "MySubscription" | Select-AzSubscription выбрать другую подписку.</span><span class="sxs-lookup"><span data-stu-id="af650-108">There is no parameter for subscription name, because it is expected for the user to specify the default subscription of the Azure login session or execute Get-AzSubscription -SubscriptionName "MySubscription" | Select-AzSubscription to select another subscription.</span></span>

## <span data-ttu-id="af650-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="af650-109">EXAMPLES</span></span>

### <span data-ttu-id="af650-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="af650-110">Example 1</span></span>
```
PS C:\> New-AzDataMigrationService -ResourceGroupName myResourceGroup -Name TestService -Location "Central US" -Sku Basic_2vCores -VirtualSubnetId $virtualSubNetId
```

<span data-ttu-id="af650-111">В примере выше показано, как создать новый экземпляр службы миграции баз данных Azure с именем TestService в центральной части США.</span><span class="sxs-lookup"><span data-stu-id="af650-111">The above example shows how to create a new instance of the Azure Database Migration Service named TestService in Central US region.</span></span>

## <span data-ttu-id="af650-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af650-112">PARAMETERS</span></span>

### <span data-ttu-id="af650-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af650-113">-DefaultProfile</span></span>
<span data-ttu-id="af650-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="af650-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af650-115">-Location</span><span class="sxs-lookup"><span data-stu-id="af650-115">-Location</span></span>
<span data-ttu-id="af650-116">Расположение экземпляра службы миграции баз данных Azure, соответствующего региону Azure.</span><span class="sxs-lookup"><span data-stu-id="af650-116">The location of the Azure Database Migration Service instance to be created, which corresponds to an Azure region.</span></span>

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

### <span data-ttu-id="af650-117">-Name</span><span class="sxs-lookup"><span data-stu-id="af650-117">-Name</span></span>
<span data-ttu-id="af650-118">Имя службы миграции базы данных.</span><span class="sxs-lookup"><span data-stu-id="af650-118">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="af650-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af650-119">-ResourceGroupName</span></span>
<span data-ttu-id="af650-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="af650-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="af650-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="af650-121">-Sku</span></span>
<span data-ttu-id="af650-122">SKU экземпляра службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="af650-122">The sku for the Azure Database Migration Service instance.</span></span> <span data-ttu-id="af650-123">Возможные значения в настоящее время Basic_1vCore, Basic_2vCores GeneralPurpose_4vCores</span><span class="sxs-lookup"><span data-stu-id="af650-123">Possible values currently are Basic_1vCore,Basic_2vCores,GeneralPurpose_4vCores</span></span>

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

### <span data-ttu-id="af650-124">-VirtualSubnetId</span><span class="sxs-lookup"><span data-stu-id="af650-124">-VirtualSubnetId</span></span>
<span data-ttu-id="af650-125">Имя подсети в указанной виртуальной сети, которая будет использовать для экземпляра службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="af650-125">The name of the subnet under the specified virtual network to use for the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="af650-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af650-126">-Confirm</span></span>
<span data-ttu-id="af650-127">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="af650-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af650-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af650-128">-WhatIf</span></span>
<span data-ttu-id="af650-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af650-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="af650-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="af650-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af650-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af650-131">CommonParameters</span></span>
<span data-ttu-id="af650-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af650-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af650-133">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af650-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af650-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="af650-134">INPUTS</span></span>

### <span data-ttu-id="af650-135">Нет</span><span class="sxs-lookup"><span data-stu-id="af650-135">None</span></span>

## <span data-ttu-id="af650-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="af650-136">OUTPUTS</span></span>

### <span data-ttu-id="af650-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="af650-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="af650-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="af650-138">NOTES</span></span>

## <span data-ttu-id="af650-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="af650-139">RELATED LINKS</span></span>
