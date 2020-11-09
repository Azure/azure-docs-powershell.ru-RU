---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationService.md
ms.openlocfilehash: 287e4db59ae19efec604da9b63958b5ea74b747f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313196"
---
# <span data-ttu-id="7628d-101">Get-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="7628d-101">Get-AzDataMigrationService</span></span>

## <span data-ttu-id="7628d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7628d-102">SYNOPSIS</span></span>
<span data-ttu-id="7628d-103">Извлекает свойства, связанные с экземпляром службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="7628d-103">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

## <span data-ttu-id="7628d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7628d-104">SYNTAX</span></span>

### <span data-ttu-id="7628d-105">ResourceGroupSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7628d-105">ResourceGroupSet (Default)</span></span>
```
Get-AzDataMigrationService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7628d-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7628d-106">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7628d-107">ServiceNameGroupSet</span><span class="sxs-lookup"><span data-stu-id="7628d-107">ServiceNameGroupSet</span></span>
```
Get-AzDataMigrationService [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7628d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7628d-108">DESCRIPTION</span></span>
<span data-ttu-id="7628d-109">Командлет Get-AzDataMigrationService извлекает свойства, связанные с экземпляром службы миграции баз данных Azure, на основе имени службы и имени группы ресурсов Azure в качестве входных параметров.</span><span class="sxs-lookup"><span data-stu-id="7628d-109">The Get-AzDataMigrationService cmdlet retrieves the properties associated with an instance of the Azure Database Migration Service based on Service name and Azure Resource Group name as input parameters.</span></span> 

## <span data-ttu-id="7628d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7628d-110">EXAMPLES</span></span>

### <span data-ttu-id="7628d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7628d-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationService -ResourceGroupName testResourceGroup -Name testService
```

<span data-ttu-id="7628d-112">В приведенном выше примере извлекаются свойства экземпляра службы миграции баз данных Azure с именем testService.</span><span class="sxs-lookup"><span data-stu-id="7628d-112">The above example retrieves the properties of the Azure Database Migration Service instance called testService.</span></span> 

### <span data-ttu-id="7628d-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7628d-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationService -ResourceGroupName testResourceGroup
```

<span data-ttu-id="7628d-114">В приведенном выше примере выполняется получение служб миграции баз данных Azure в группе ресурсов с именем testResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7628d-114">The above example retrieves Azure Database Migration Services in the resource group called testResourceGroup.</span></span> 

## <span data-ttu-id="7628d-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7628d-115">PARAMETERS</span></span>

### <span data-ttu-id="7628d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7628d-116">-DefaultProfile</span></span>
<span data-ttu-id="7628d-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7628d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7628d-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7628d-118">-Name</span></span>
<span data-ttu-id="7628d-119">Имя службы миграции баз данных.</span><span class="sxs-lookup"><span data-stu-id="7628d-119">Name of Database Migration Service.</span></span>

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

### <span data-ttu-id="7628d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7628d-120">-ResourceGroupName</span></span>
<span data-ttu-id="7628d-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7628d-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="7628d-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7628d-122">-ResourceId</span></span>
<span data-ttu-id="7628d-123">Идентификатор ресурса DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="7628d-123">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="7628d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7628d-124">CommonParameters</span></span>
<span data-ttu-id="7628d-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7628d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7628d-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7628d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7628d-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7628d-127">INPUTS</span></span>

### <span data-ttu-id="7628d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7628d-128">System.String</span></span>

## <span data-ttu-id="7628d-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7628d-129">OUTPUTS</span></span>

### <span data-ttu-id="7628d-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="7628d-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="7628d-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="7628d-131">NOTES</span></span>

## <span data-ttu-id="7628d-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7628d-132">RELATED LINKS</span></span>
