---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Get-AzureRmDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationProject.md
ms.openlocfilehash: 31d37f740500247fed433c3e40b9d8220a5af663
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566479"
---
# <span data-ttu-id="5f5c6-101">Get-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="5f5c6-101">Get-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="5f5c6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5f5c6-102">SYNOPSIS</span></span>
<span data-ttu-id="5f5c6-103">Извлекает свойства проекта миграции базы данных Azure.</span><span class="sxs-lookup"><span data-stu-id="5f5c6-103">Retrieves the properties of an Azure Database Migration project.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f5c6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5f5c6-104">SYNTAX</span></span>

### <span data-ttu-id="5f5c6-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5f5c6-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f5c6-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f5c6-106">ComponentObjectParameterSet</span></span>
```
Get-AzureRmDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f5c6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f5c6-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmDataMigrationProject [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f5c6-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f5c6-108">DESCRIPTION</span></span>
<span data-ttu-id="5f5c6-109">Командлет Get-AzureRmDataMigrationProject извлекает свойства проекта миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="5f5c6-109">The Get-AzureRmDataMigrationProject cmdlet retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="5f5c6-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5f5c6-110">EXAMPLES</span></span>

### <span data-ttu-id="5f5c6-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5f5c6-111">Example 1</span></span>
```
PS C:\> Get-AzureRmDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

<span data-ttu-id="5f5c6-112">В приведенном выше примере выполняется получение проекта миграции базы данных Azure с именем TestProject в группе ресурсов под названием testResourceGroup и в разделе Служба под названием testService</span><span class="sxs-lookup"><span data-stu-id="5f5c6-112">The above example retrieves  Azure Database Migration project named TestProject in the resource group called testResourceGroup and under service called testService</span></span>

### <span data-ttu-id="5f5c6-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5f5c6-113">Example 2</span></span>
```
PS C:\> Get-AzureRmDataMigrationProject -InputObject $myService
```

<span data-ttu-id="5f5c6-114">В приведенном выше примере выполняется получение проекта миграции базы данных Azure на основе переданного входного параметра объекта PSProject.</span><span class="sxs-lookup"><span data-stu-id="5f5c6-114">The above example retrieves the  Azure Database Migration project based on PSProject object input parameter passed in.</span></span> 

## <span data-ttu-id="5f5c6-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5f5c6-115">PARAMETERS</span></span>

### <span data-ttu-id="5f5c6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f5c6-116">-DefaultProfile</span></span>
<span data-ttu-id="5f5c6-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5f5c6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f5c6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5f5c6-118">-InputObject</span></span>
<span data-ttu-id="5f5c6-119">Объект PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="5f5c6-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="5f5c6-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5f5c6-120">-Name</span></span>
<span data-ttu-id="5f5c6-121">Имя проекта.</span><span class="sxs-lookup"><span data-stu-id="5f5c6-121">The name of the project.</span></span>

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

### <span data-ttu-id="5f5c6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f5c6-122">-ResourceGroupName</span></span>
<span data-ttu-id="5f5c6-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5f5c6-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="5f5c6-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5f5c6-124">-ResourceId</span></span>
<span data-ttu-id="5f5c6-125">Идентификатор ресурса DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="5f5c6-125">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="5f5c6-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="5f5c6-126">-ServiceName</span></span>
<span data-ttu-id="5f5c6-127">Имя службы миграции баз данных.</span><span class="sxs-lookup"><span data-stu-id="5f5c6-127">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="5f5c6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f5c6-128">CommonParameters</span></span>
<span data-ttu-id="5f5c6-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5f5c6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f5c6-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f5c6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f5c6-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5f5c6-131">INPUTS</span></span>

### <span data-ttu-id="5f5c6-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="5f5c6-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="5f5c6-133">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5f5c6-133">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="5f5c6-134">System. String</span><span class="sxs-lookup"><span data-stu-id="5f5c6-134">System.String</span></span>

## <span data-ttu-id="5f5c6-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f5c6-135">OUTPUTS</span></span>

### <span data-ttu-id="5f5c6-136">Microsoft. Azure. Commands. Migration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="5f5c6-136">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="5f5c6-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="5f5c6-137">NOTES</span></span>

## <span data-ttu-id="5f5c6-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5f5c6-138">RELATED LINKS</span></span>
