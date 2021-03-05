---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationService.md
ms.openlocfilehash: 7d36860991d5b6b12fb23044cc607044fb87bfa6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010616"
---
# <span data-ttu-id="dfdd6-101">New-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="dfdd6-101">New-AzDataMigrationService</span></span>

## <span data-ttu-id="dfdd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfdd6-102">SYNOPSIS</span></span>
<span data-ttu-id="dfdd6-103">Создает новый экземпляр службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="dfdd6-103">Creates a new instance of the Azure Database Migration Service.</span></span>

## <span data-ttu-id="dfdd6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dfdd6-104">SYNTAX</span></span>

```
New-AzDataMigrationService -ResourceGroupName <String> -Name <String> -Location <String> -Sku <String>
 -VirtualSubnetId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfdd6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dfdd6-105">DESCRIPTION</span></span>
<span data-ttu-id="dfdd6-106">С New-AzDataMigrationService создается новый экземпляр службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="dfdd6-106">The New-AzDataMigrationService cmdlet creates a new instance of the Azure Database Migration Service.</span></span> <span data-ttu-id="dfdd6-107">Этот cmdlet принимает имя существующей группы ресурсов Azure, уникальное имя нового экземпляра службы миграции баз данных Azure, регион, в котором он предусмотрен, имя SKU "Сотрудник DMS" и имя виртуальной подсети Azure, в которой должна находиться служба.</span><span class="sxs-lookup"><span data-stu-id="dfdd6-107">This cmdlet takes in name of existing Azure Resource Group, the unique name for the new instance of the Azure Database Migration Service to be created, the region in which the instance is provisioned, the name of the DMS Worker SKU, and the name of the Azure Virtual Subnet on which the service is to reside.</span></span> <span data-ttu-id="dfdd6-108">Параметр для имени подписки не задан, так как предполагается, что пользователь указывает стандартную подписку на сеанс входа Azure или выполняет Get-AzSubscription -SubscriptionName "MySubscription" | Select-AzSubscription выбрать другую подписку.</span><span class="sxs-lookup"><span data-stu-id="dfdd6-108">There is no parameter for subscription name, because it is expected for the user to specify the default subscription of the Azure login session or execute Get-AzSubscription -SubscriptionName "MySubscription" | Select-AzSubscription to select another subscription.</span></span>

## <span data-ttu-id="dfdd6-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dfdd6-109">EXAMPLES</span></span>

### <span data-ttu-id="dfdd6-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dfdd6-110">Example 1</span></span>
```
PS C:\> New-AzDataMigrationService -ResourceGroupName myResourceGroup -Name TestService -Location "Central US" -Sku Basic_2vCores -VirtualSubnetId $virtualSubNetId
```

<span data-ttu-id="dfdd6-111">В примере выше показано, как создать новый экземпляр службы миграции баз данных Azure с именем TestService в центральной части США.</span><span class="sxs-lookup"><span data-stu-id="dfdd6-111">The above example shows how to create a new instance of the Azure Database Migration Service named TestService in Central US region.</span></span>

## <span data-ttu-id="dfdd6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dfdd6-112">PARAMETERS</span></span>

### <span data-ttu-id="dfdd6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfdd6-113">-DefaultProfile</span></span>
<span data-ttu-id="dfdd6-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dfdd6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfdd6-115">-Location</span><span class="sxs-lookup"><span data-stu-id="dfdd6-115">-Location</span></span>
<span data-ttu-id="dfdd6-116">Расположение экземпляра службы миграции баз данных Azure, соответствующего региону Azure.</span><span class="sxs-lookup"><span data-stu-id="dfdd6-116">The location of the Azure Database Migration Service instance to be created, which corresponds to an Azure region.</span></span>

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

### <span data-ttu-id="dfdd6-117">-Name</span><span class="sxs-lookup"><span data-stu-id="dfdd6-117">-Name</span></span>
<span data-ttu-id="dfdd6-118">Имя службы миграции базы данных.</span><span class="sxs-lookup"><span data-stu-id="dfdd6-118">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="dfdd6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfdd6-119">-ResourceGroupName</span></span>
<span data-ttu-id="dfdd6-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dfdd6-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="dfdd6-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="dfdd6-121">-Sku</span></span>
<span data-ttu-id="dfdd6-122">SKU экземпляра службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="dfdd6-122">The sku for the Azure Database Migration Service instance.</span></span> <span data-ttu-id="dfdd6-123">Возможные значения в настоящее время Basic_1vCore, Basic_2vCores GeneralPurpose_4vCores</span><span class="sxs-lookup"><span data-stu-id="dfdd6-123">Possible values currently are Basic_1vCore,Basic_2vCores,GeneralPurpose_4vCores</span></span>

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

### <span data-ttu-id="dfdd6-124">-VirtualSubnetId</span><span class="sxs-lookup"><span data-stu-id="dfdd6-124">-VirtualSubnetId</span></span>
<span data-ttu-id="dfdd6-125">Имя подсети в указанной виртуальной сети, используемой для экземпляра службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="dfdd6-125">The name of the subnet under the specified virtual network to use for the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="dfdd6-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dfdd6-126">-Confirm</span></span>
<span data-ttu-id="dfdd6-127">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfdd6-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfdd6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfdd6-128">-WhatIf</span></span>
<span data-ttu-id="dfdd6-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfdd6-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dfdd6-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="dfdd6-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfdd6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfdd6-131">CommonParameters</span></span>
<span data-ttu-id="dfdd6-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfdd6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfdd6-133">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfdd6-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfdd6-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dfdd6-134">INPUTS</span></span>

### <span data-ttu-id="dfdd6-135">Нет</span><span class="sxs-lookup"><span data-stu-id="dfdd6-135">None</span></span>

## <span data-ttu-id="dfdd6-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dfdd6-136">OUTPUTS</span></span>

### <span data-ttu-id="dfdd6-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="dfdd6-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="dfdd6-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dfdd6-138">NOTES</span></span>

## <span data-ttu-id="dfdd6-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dfdd6-139">RELATED LINKS</span></span>
