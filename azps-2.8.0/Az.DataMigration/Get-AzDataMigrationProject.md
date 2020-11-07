---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
ms.openlocfilehash: 00a0e0a688f49615cadff3990071cd49d1356443
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721256"
---
# <span data-ttu-id="3bbd4-101">Get-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="3bbd4-101">Get-AzDataMigrationProject</span></span>

## <span data-ttu-id="3bbd4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3bbd4-102">SYNOPSIS</span></span>
<span data-ttu-id="3bbd4-103">Извлекает свойства проекта миграции базы данных Azure.</span><span class="sxs-lookup"><span data-stu-id="3bbd4-103">Retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="3bbd4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3bbd4-104">SYNTAX</span></span>

### <span data-ttu-id="3bbd4-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3bbd4-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bbd4-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bbd4-106">ComponentObjectParameterSet</span></span>
```
Get-AzDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bbd4-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bbd4-107">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationProject [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3bbd4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3bbd4-108">DESCRIPTION</span></span>
<span data-ttu-id="3bbd4-109">Командлет Get-AzDataMigrationProject извлекает свойства проекта миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="3bbd4-109">The Get-AzDataMigrationProject cmdlet retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="3bbd4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3bbd4-110">EXAMPLES</span></span>

### <span data-ttu-id="3bbd4-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3bbd4-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

<span data-ttu-id="3bbd4-112">В приведенном выше примере выполняется получение проекта миграции базы данных Azure с именем TestProject в группе ресурсов под названием testResourceGroup и в разделе Служба под названием testService</span><span class="sxs-lookup"><span data-stu-id="3bbd4-112">The above example retrieves  Azure Database Migration project named TestProject in the resource group called testResourceGroup and under service called testService</span></span>

### <span data-ttu-id="3bbd4-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3bbd4-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationProject -InputObject $myService
```

<span data-ttu-id="3bbd4-114">В приведенном выше примере выполняется получение проекта миграции базы данных Azure на основе переданного входного параметра объекта PSProject.</span><span class="sxs-lookup"><span data-stu-id="3bbd4-114">The above example retrieves the  Azure Database Migration project based on PSProject object input parameter passed in.</span></span> 

## <span data-ttu-id="3bbd4-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3bbd4-115">PARAMETERS</span></span>

### <span data-ttu-id="3bbd4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bbd4-116">-DefaultProfile</span></span>
<span data-ttu-id="3bbd4-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3bbd4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3bbd4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3bbd4-118">-InputObject</span></span>
<span data-ttu-id="3bbd4-119">Объект PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="3bbd4-119">PSDataMigrationService Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3bbd4-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3bbd4-120">-Name</span></span>
<span data-ttu-id="3bbd4-121">Имя проекта.</span><span class="sxs-lookup"><span data-stu-id="3bbd4-121">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProjectName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bbd4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bbd4-122">-ResourceGroupName</span></span>
<span data-ttu-id="3bbd4-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3bbd4-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bbd4-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3bbd4-124">-ResourceId</span></span>
<span data-ttu-id="3bbd4-125">Идентификатор ресурса DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="3bbd4-125">DataMigrationService Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bbd4-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3bbd4-126">-ServiceName</span></span>
<span data-ttu-id="3bbd4-127">Имя службы миграции баз данных.</span><span class="sxs-lookup"><span data-stu-id="3bbd4-127">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bbd4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bbd4-128">CommonParameters</span></span>
<span data-ttu-id="3bbd4-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3bbd4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bbd4-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bbd4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bbd4-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3bbd4-131">INPUTS</span></span>

### <span data-ttu-id="3bbd4-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="3bbd4-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="3bbd4-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3bbd4-133">System.String</span></span>

## <span data-ttu-id="3bbd4-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3bbd4-134">OUTPUTS</span></span>

### <span data-ttu-id="3bbd4-135">Microsoft. Azure. Commands. Migration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="3bbd4-135">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="3bbd4-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="3bbd4-136">NOTES</span></span>

## <span data-ttu-id="3bbd4-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3bbd4-137">RELATED LINKS</span></span>
