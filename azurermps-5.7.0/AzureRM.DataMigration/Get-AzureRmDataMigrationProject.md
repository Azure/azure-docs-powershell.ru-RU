---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/get-azurermdatamigrationproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationProject.md
ms.openlocfilehash: ea6406d83004d9a7d21a2f47aba0c39a10caf59a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568009"
---
# <span data-ttu-id="92aaa-101">Get-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="92aaa-101">Get-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="92aaa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="92aaa-102">SYNOPSIS</span></span>
<span data-ttu-id="92aaa-103">Извлекает свойства проекта миграции базы данных Azure.</span><span class="sxs-lookup"><span data-stu-id="92aaa-103">Retrieves the properties of an Azure Database Migration project.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92aaa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="92aaa-104">SYNTAX</span></span>

### <span data-ttu-id="92aaa-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="92aaa-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="92aaa-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="92aaa-106">ComponentObjectParameterSet</span></span>
```
Get-AzureRmDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="92aaa-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="92aaa-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmDataMigrationProject [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="92aaa-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="92aaa-108">DESCRIPTION</span></span>
<span data-ttu-id="92aaa-109">Командлет Get-AzureRmDataMigrationProject извлекает свойства проекта миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="92aaa-109">The Get-AzureRmDataMigrationProject cmdlet retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="92aaa-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="92aaa-110">EXAMPLES</span></span>

### <span data-ttu-id="92aaa-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="92aaa-111">Example 1</span></span>
```
PS C:\> Get-AzureRmDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

<span data-ttu-id="92aaa-112">В приведенном выше примере выполняется получение проекта миграции базы данных Azure с именем TestProject в группе ресурсов под названием testResourceGroup и в разделе Служба под названием testService</span><span class="sxs-lookup"><span data-stu-id="92aaa-112">The above example retrieves  Azure Database Migration project named TestProject in the resource group called testResourceGroup and under service called testService</span></span>

### <span data-ttu-id="92aaa-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="92aaa-113">Example 2</span></span>
```
PS C:\> Get-AzureRmDataMigrationProject -InputObject $myService
```

<span data-ttu-id="92aaa-114">В приведенном выше примере выполняется получение проекта миграции базы данных Azure на основе переданного входного параметра объекта PSProject.</span><span class="sxs-lookup"><span data-stu-id="92aaa-114">The above example retrieves the  Azure Database Migration project based on PSProject object input parameter passed in.</span></span> 


## <span data-ttu-id="92aaa-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="92aaa-115">PARAMETERS</span></span>

### <span data-ttu-id="92aaa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92aaa-116">-DefaultProfile</span></span>
<span data-ttu-id="92aaa-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="92aaa-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92aaa-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92aaa-118">-InputObject</span></span>
<span data-ttu-id="92aaa-119">Объект PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="92aaa-119">PSDataMigrationService Object.</span></span>

```yaml
Type: PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92aaa-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="92aaa-120">-Name</span></span>
<span data-ttu-id="92aaa-121">Имя проекта.</span><span class="sxs-lookup"><span data-stu-id="92aaa-121">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ProjectName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92aaa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92aaa-122">-ResourceGroupName</span></span>
<span data-ttu-id="92aaa-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="92aaa-123">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92aaa-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92aaa-124">-ResourceId</span></span>
<span data-ttu-id="92aaa-125">Идентификатор ресурса DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="92aaa-125">DataMigrationService Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92aaa-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="92aaa-126">-ServiceName</span></span>
<span data-ttu-id="92aaa-127">Имя службы миграции данных.</span><span class="sxs-lookup"><span data-stu-id="92aaa-127">Data Migration Service Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="92aaa-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="92aaa-128">INPUTS</span></span>

### <span data-ttu-id="92aaa-129">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="92aaa-129">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="92aaa-130">System. String</span><span class="sxs-lookup"><span data-stu-id="92aaa-130">System.String</span></span>


## <span data-ttu-id="92aaa-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="92aaa-131">OUTPUTS</span></span>

### <span data-ttu-id="92aaa-132">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. Migration. Models. PSProject, Microsoft. Azure. Commands. DataCulture, версия = 0.1.0.0, культура = нейтральная, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="92aaa-132">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.DataMigration.Models.PSProject, Microsoft.Azure.Commands.DataMigration, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="92aaa-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="92aaa-133">NOTES</span></span>

## <span data-ttu-id="92aaa-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="92aaa-134">RELATED LINKS</span></span>

