---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationService.md
ms.openlocfilehash: 287e4db59ae19efec604da9b63958b5ea74b747f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504534"
---
# <span data-ttu-id="00e76-101">Get-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="00e76-101">Get-AzDataMigrationService</span></span>

## <span data-ttu-id="00e76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00e76-102">SYNOPSIS</span></span>
<span data-ttu-id="00e76-103">Извлекает свойства, связанные с экземпляром службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="00e76-103">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

## <span data-ttu-id="00e76-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="00e76-104">SYNTAX</span></span>

### <span data-ttu-id="00e76-105">ResourceGroupSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="00e76-105">ResourceGroupSet (Default)</span></span>
```
Get-AzDataMigrationService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="00e76-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="00e76-106">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="00e76-107">ServiceNameGroupSet</span><span class="sxs-lookup"><span data-stu-id="00e76-107">ServiceNameGroupSet</span></span>
```
Get-AzDataMigrationService [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00e76-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="00e76-108">DESCRIPTION</span></span>
<span data-ttu-id="00e76-109">С Get-AzDataMigrationService- именем группы ресурсов Azure в качестве входных параметров извлекает свойства, связанные с экземпляром службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="00e76-109">The Get-AzDataMigrationService cmdlet retrieves the properties associated with an instance of the Azure Database Migration Service based on Service name and Azure Resource Group name as input parameters.</span></span> 

## <span data-ttu-id="00e76-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="00e76-110">EXAMPLES</span></span>

### <span data-ttu-id="00e76-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="00e76-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationService -ResourceGroupName testResourceGroup -Name testService
```

<span data-ttu-id="00e76-112">В примере выше извлекались свойства экземпляра службы миграции баз данных Azure, который называется testService.</span><span class="sxs-lookup"><span data-stu-id="00e76-112">The above example retrieves the properties of the Azure Database Migration Service instance called testService.</span></span> 

### <span data-ttu-id="00e76-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="00e76-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationService -ResourceGroupName testResourceGroup
```

<span data-ttu-id="00e76-114">В примере выше извлекаются службы миграции баз данных Azure в группе ресурсов testResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="00e76-114">The above example retrieves Azure Database Migration Services in the resource group called testResourceGroup.</span></span> 

## <span data-ttu-id="00e76-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00e76-115">PARAMETERS</span></span>

### <span data-ttu-id="00e76-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00e76-116">-DefaultProfile</span></span>
<span data-ttu-id="00e76-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="00e76-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00e76-118">-Name</span><span class="sxs-lookup"><span data-stu-id="00e76-118">-Name</span></span>
<span data-ttu-id="00e76-119">Имя службы миграции баз данных.</span><span class="sxs-lookup"><span data-stu-id="00e76-119">Name of Database Migration Service.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameGroupSet
Aliases: ServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00e76-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00e76-120">-ResourceGroupName</span></span>
<span data-ttu-id="00e76-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="00e76-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServiceNameGroupSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00e76-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00e76-122">-ResourceId</span></span>
<span data-ttu-id="00e76-123">DataMigrationService Resource Id.</span><span class="sxs-lookup"><span data-stu-id="00e76-123">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="00e76-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00e76-124">CommonParameters</span></span>
<span data-ttu-id="00e76-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00e76-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00e76-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00e76-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00e76-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="00e76-127">INPUTS</span></span>

### <span data-ttu-id="00e76-128">System.String</span><span class="sxs-lookup"><span data-stu-id="00e76-128">System.String</span></span>

## <span data-ttu-id="00e76-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="00e76-129">OUTPUTS</span></span>

### <span data-ttu-id="00e76-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="00e76-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="00e76-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="00e76-131">NOTES</span></span>

## <span data-ttu-id="00e76-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="00e76-132">RELATED LINKS</span></span>
