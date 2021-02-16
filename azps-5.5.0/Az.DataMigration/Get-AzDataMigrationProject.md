---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
ms.openlocfilehash: 7fe1e12c7c7feb2a47ac33b309b188e53e77fc73
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238163"
---
# <span data-ttu-id="1270f-101">Get-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="1270f-101">Get-AzDataMigrationProject</span></span>

## <span data-ttu-id="1270f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1270f-102">SYNOPSIS</span></span>
<span data-ttu-id="1270f-103">Извлекает свойства проекта миграции базы данных Azure.</span><span class="sxs-lookup"><span data-stu-id="1270f-103">Retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="1270f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1270f-104">SYNTAX</span></span>

### <span data-ttu-id="1270f-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1270f-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1270f-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1270f-106">ComponentObjectParameterSet</span></span>
```
Get-AzDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1270f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1270f-107">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationProject [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1270f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1270f-108">DESCRIPTION</span></span>
<span data-ttu-id="1270f-109">С Get-AzDataMigrationProject-частью можно получить свойства проекта миграции базы данных Azure.</span><span class="sxs-lookup"><span data-stu-id="1270f-109">The Get-AzDataMigrationProject cmdlet retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="1270f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1270f-110">EXAMPLES</span></span>

### <span data-ttu-id="1270f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1270f-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

<span data-ttu-id="1270f-112">В примере выше извлекается проект миграции базы данных Azure с именем TestProject в группе ресурсов testResourceGroup и под службой testService.</span><span class="sxs-lookup"><span data-stu-id="1270f-112">The above example retrieves  Azure Database Migration project named TestProject in the resource group called testResourceGroup and under service called testService</span></span>

### <span data-ttu-id="1270f-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="1270f-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationProject -InputObject $myService
```

<span data-ttu-id="1270f-114">В примере выше извлекается проект миграции базы данных Azure на основе переданного параметра ввода объекта PSProject.</span><span class="sxs-lookup"><span data-stu-id="1270f-114">The above example retrieves the  Azure Database Migration project based on PSProject object input parameter passed in.</span></span> 

## <span data-ttu-id="1270f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1270f-115">PARAMETERS</span></span>

### <span data-ttu-id="1270f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1270f-116">-DefaultProfile</span></span>
<span data-ttu-id="1270f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1270f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1270f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1270f-118">-InputObject</span></span>
<span data-ttu-id="1270f-119">Объект PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="1270f-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="1270f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="1270f-120">-Name</span></span>
<span data-ttu-id="1270f-121">Название проекта.</span><span class="sxs-lookup"><span data-stu-id="1270f-121">The name of the project.</span></span>

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

### <span data-ttu-id="1270f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1270f-122">-ResourceGroupName</span></span>
<span data-ttu-id="1270f-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1270f-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="1270f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1270f-124">-ResourceId</span></span>
<span data-ttu-id="1270f-125">DataMigrationService Resource Id.</span><span class="sxs-lookup"><span data-stu-id="1270f-125">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="1270f-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="1270f-126">-ServiceName</span></span>
<span data-ttu-id="1270f-127">Имя службы миграции базы данных.</span><span class="sxs-lookup"><span data-stu-id="1270f-127">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="1270f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1270f-128">CommonParameters</span></span>
<span data-ttu-id="1270f-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1270f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1270f-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1270f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1270f-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1270f-131">INPUTS</span></span>

### <span data-ttu-id="1270f-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="1270f-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="1270f-133">System.String</span><span class="sxs-lookup"><span data-stu-id="1270f-133">System.String</span></span>

## <span data-ttu-id="1270f-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1270f-134">OUTPUTS</span></span>

### <span data-ttu-id="1270f-135">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="1270f-135">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="1270f-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1270f-136">NOTES</span></span>

## <span data-ttu-id="1270f-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1270f-137">RELATED LINKS</span></span>
