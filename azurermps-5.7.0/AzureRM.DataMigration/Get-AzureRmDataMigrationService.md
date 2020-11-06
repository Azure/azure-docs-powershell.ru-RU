---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/get-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationService.md
ms.openlocfilehash: cac57ff34d925d553c25d97facd81dba017a25c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566186"
---
# <span data-ttu-id="fddc8-101">Get-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="fddc8-101">Get-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="fddc8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fddc8-102">SYNOPSIS</span></span>
<span data-ttu-id="fddc8-103">Извлекает свойства, связанные с экземпляром службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="fddc8-103">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fddc8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fddc8-104">SYNTAX</span></span>

### <span data-ttu-id="fddc8-105">ResourceGroupSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fddc8-105">ResourceGroupSet (Default)</span></span>
```
Get-AzureRmDataMigrationService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="fddc8-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fddc8-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmDataMigrationService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="fddc8-107">ServiceNameGroupSet</span><span class="sxs-lookup"><span data-stu-id="fddc8-107">ServiceNameGroupSet</span></span>
```
Get-AzureRmDataMigrationService [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>]
```
## <span data-ttu-id="fddc8-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fddc8-108">DESCRIPTION</span></span>
<span data-ttu-id="fddc8-109">Командлет Get-AzureRmDataMigrationService извлекает свойства, связанные с экземпляром службы миграции баз данных Azure, на основе имени службы и имени группы ресурсов Azure в качестве входных параметров.</span><span class="sxs-lookup"><span data-stu-id="fddc8-109">The Get-AzureRmDataMigrationService cmdlet retrieves the properties associated with an instance of the Azure Database Migration Service based on Service name and Azure Resource Group name as input parameters.</span></span> 

## <span data-ttu-id="fddc8-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fddc8-110">EXAMPLES</span></span>

### <span data-ttu-id="fddc8-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fddc8-111">Example 1</span></span>
```
PS C:\> Get-AzureRmDataMigrationService -ResourceGroupName testResourceGroup -Name testService
```

<span data-ttu-id="fddc8-112">В приведенном выше примере извлекаются свойства экземпляра службы миграции баз данных Azure с именем testService.</span><span class="sxs-lookup"><span data-stu-id="fddc8-112">The above example retrieves the properties of the Azure Database Migration Service instance called testService.</span></span> 

### <span data-ttu-id="fddc8-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="fddc8-113">Example 2</span></span>
```
PS C:\> Get-AzureRmDataMigrationService -ResourceGroupName testResourceGroup 
```

<span data-ttu-id="fddc8-114">В приведенном выше примере выполняется получение служб миграции баз данных Azure в группе ресурсов с именем testResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fddc8-114">The above example retrieves Azure Database Migration Services in the resource group called testResourceGroup.</span></span> 

## <span data-ttu-id="fddc8-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fddc8-115">PARAMETERS</span></span>

### <span data-ttu-id="fddc8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fddc8-116">-DefaultProfile</span></span>
<span data-ttu-id="fddc8-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fddc8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fddc8-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fddc8-118">-Name</span></span>
<span data-ttu-id="fddc8-119">Имя службы миграции данных.</span><span class="sxs-lookup"><span data-stu-id="fddc8-119">Name of Data Migration Service.</span></span>

```yaml
Type: String
Parameter Sets: ServiceNameGroupSet
Aliases: ServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fddc8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fddc8-120">-ResourceGroupName</span></span>
<span data-ttu-id="fddc8-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fddc8-121">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServiceNameGroupSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fddc8-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fddc8-122">-ResourceId</span></span>
<span data-ttu-id="fddc8-123">Идентификатор ресурса DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="fddc8-123">DataMigrationService Resource Id.</span></span>

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

## <span data-ttu-id="fddc8-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fddc8-124">INPUTS</span></span>

### <span data-ttu-id="fddc8-125">System. String</span><span class="sxs-lookup"><span data-stu-id="fddc8-125">System.String</span></span>


## <span data-ttu-id="fddc8-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fddc8-126">OUTPUTS</span></span>

### <span data-ttu-id="fddc8-127">System. Collections. Generic. IList ' 1 [[Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService, Microsoft. Azure. Commands. Migration, Version = 0.1.0.0, культура = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="fddc8-127">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService, Microsoft.Azure.Commands.DataMigration, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="fddc8-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="fddc8-128">NOTES</span></span>

## <span data-ttu-id="fddc8-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fddc8-129">RELATED LINKS</span></span>





