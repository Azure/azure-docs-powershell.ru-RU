---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
ms.openlocfilehash: cc2f708294be05b16b0c5be94fb9da260b479799
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566473"
---
# <span data-ttu-id="e35fb-101">New-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="e35fb-101">New-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="e35fb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e35fb-102">SYNOPSIS</span></span>
<span data-ttu-id="e35fb-103">Создание нового экземпляра службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="e35fb-103">Creates a new instance of the Azure Database Migration Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e35fb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e35fb-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> -Location <String> -Sku <String>
 -VirtualSubnetId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e35fb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e35fb-105">DESCRIPTION</span></span>
<span data-ttu-id="e35fb-106">Командлет New-AzureRmDataMigrationService создает новый экземпляр службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="e35fb-106">The New-AzureRmDataMigrationService cmdlet creates a new instance of the Azure Database Migration Service.</span></span> <span data-ttu-id="e35fb-107">Этот командлет принимает имя существующей группы ресурсов Azure, уникальное имя для нового экземпляра службы миграции баз данных Azure, область, в которой выполняется подготовка экземпляра, имя SKU рабочего процесса DMS и имя виртуальной подсети Azure, в которой будет находиться служба.</span><span class="sxs-lookup"><span data-stu-id="e35fb-107">This cmdlet takes in name of existing Azure Resource Group, the unique name for the new instance of the Azure Database Migration Service to be created, the region in which the instance is provisioned, the name of the DMS Worker SKU, and the name of the Azure Virtual Subnet on which the service is to reside.</span></span> <span data-ttu-id="e35fb-108">Для имени подписки нет параметра, так как ожидается, что пользователь должен указать подписку по умолчанию для сеанса входа Azure или выполнить Get-AzureRmSubscription-SubscriptionName "MySubscription" | Select-AzureRmSubscription, чтобы выбрать другую подписку.</span><span class="sxs-lookup"><span data-stu-id="e35fb-108">There is no parameter for subscription name, because it is expected for the user to specify the default subscription of the Azure login session or execute Get-AzureRmSubscription -SubscriptionName "MySubscription" | Select-AzureRmSubscription to select another subscription.</span></span>

## <span data-ttu-id="e35fb-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e35fb-109">EXAMPLES</span></span>

### <span data-ttu-id="e35fb-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e35fb-110">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationService -ResourceGroupName myResourceGroup -Name TestService -Location "Central US" -Sku Basic_2vCores -VirtualSubnetId $virtualSubNetId
```

<span data-ttu-id="e35fb-111">В приведенном выше примере показано, как создать новый экземпляр службы миграции баз данных Azure с именем TestService в центральном регионе США.</span><span class="sxs-lookup"><span data-stu-id="e35fb-111">The above example shows how to create a new instance of the Azure Database Migration Service named TestService in Central US region.</span></span>

## <span data-ttu-id="e35fb-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e35fb-112">PARAMETERS</span></span>

### <span data-ttu-id="e35fb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e35fb-113">-DefaultProfile</span></span>
<span data-ttu-id="e35fb-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e35fb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e35fb-115">-Location</span><span class="sxs-lookup"><span data-stu-id="e35fb-115">-Location</span></span>
<span data-ttu-id="e35fb-116">Расположение создаваемого экземпляра службы миграции баз данных Azure, которое соответствует региону Azure.</span><span class="sxs-lookup"><span data-stu-id="e35fb-116">The location of the Azure Database Migration Service instance to be created, which corresponds to an Azure region.</span></span>

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

### <span data-ttu-id="e35fb-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e35fb-117">-Name</span></span>
<span data-ttu-id="e35fb-118">Имя службы миграции баз данных.</span><span class="sxs-lookup"><span data-stu-id="e35fb-118">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="e35fb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e35fb-119">-ResourceGroupName</span></span>
<span data-ttu-id="e35fb-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e35fb-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="e35fb-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="e35fb-121">-Sku</span></span>
<span data-ttu-id="e35fb-122">SKU для экземпляра службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="e35fb-122">The sku for the Azure Database Migration Service instance.</span></span> <span data-ttu-id="e35fb-123">В настоящее время доступны значения Basic_1vCore, Basic_2vCores GeneralPurpose_4vCores</span><span class="sxs-lookup"><span data-stu-id="e35fb-123">Possible values currently are Basic_1vCore,Basic_2vCores,GeneralPurpose_4vCores</span></span>

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

### <span data-ttu-id="e35fb-124">-VirtualSubnetId</span><span class="sxs-lookup"><span data-stu-id="e35fb-124">-VirtualSubnetId</span></span>
<span data-ttu-id="e35fb-125">Имя подсети в указанной виртуальной сети, используемой для экземпляра службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="e35fb-125">The name of the subnet under the specified virtual network to use for the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="e35fb-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e35fb-126">-Confirm</span></span>
<span data-ttu-id="e35fb-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e35fb-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e35fb-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e35fb-128">-WhatIf</span></span>
<span data-ttu-id="e35fb-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e35fb-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e35fb-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e35fb-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e35fb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e35fb-131">CommonParameters</span></span>
<span data-ttu-id="e35fb-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e35fb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e35fb-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e35fb-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e35fb-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e35fb-134">INPUTS</span></span>

### <span data-ttu-id="e35fb-135">Ничего</span><span class="sxs-lookup"><span data-stu-id="e35fb-135">None</span></span>

## <span data-ttu-id="e35fb-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e35fb-136">OUTPUTS</span></span>

### <span data-ttu-id="e35fb-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="e35fb-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="e35fb-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="e35fb-138">NOTES</span></span>

## <span data-ttu-id="e35fb-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e35fb-139">RELATED LINKS</span></span>
