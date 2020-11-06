---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Get-AzureRmDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationService.md
ms.openlocfilehash: 06899e35e9119025aa13a310a3d6200c30b223df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566478"
---
# <span data-ttu-id="ad7ad-101">Get-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="ad7ad-101">Get-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="ad7ad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ad7ad-102">SYNOPSIS</span></span>
<span data-ttu-id="ad7ad-103">Извлекает свойства, связанные с экземпляром службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="ad7ad-103">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad7ad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ad7ad-104">SYNTAX</span></span>

### <span data-ttu-id="ad7ad-105">ResourceGroupSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ad7ad-105">ResourceGroupSet (Default)</span></span>
```
Get-AzureRmDataMigrationService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad7ad-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad7ad-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmDataMigrationService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad7ad-107">ServiceNameGroupSet</span><span class="sxs-lookup"><span data-stu-id="ad7ad-107">ServiceNameGroupSet</span></span>
```
Get-AzureRmDataMigrationService [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad7ad-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad7ad-108">DESCRIPTION</span></span>
<span data-ttu-id="ad7ad-109">Командлет Get-AzureRmDataMigrationService извлекает свойства, связанные с экземпляром службы миграции баз данных Azure, на основе имени службы и имени группы ресурсов Azure в качестве входных параметров.</span><span class="sxs-lookup"><span data-stu-id="ad7ad-109">The Get-AzureRmDataMigrationService cmdlet retrieves the properties associated with an instance of the Azure Database Migration Service based on Service name and Azure Resource Group name as input parameters.</span></span> 

## <span data-ttu-id="ad7ad-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ad7ad-110">EXAMPLES</span></span>

### <span data-ttu-id="ad7ad-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ad7ad-111">Example 1</span></span>
```
PS C:\> Get-AzureRmDataMigrationService -ResourceGroupName testResourceGroup -Name testService
```

<span data-ttu-id="ad7ad-112">В приведенном выше примере извлекаются свойства экземпляра службы миграции баз данных Azure с именем testService.</span><span class="sxs-lookup"><span data-stu-id="ad7ad-112">The above example retrieves the properties of the Azure Database Migration Service instance called testService.</span></span> 

### <span data-ttu-id="ad7ad-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ad7ad-113">Example 2</span></span>
```
PS C:\> Get-AzureRmDataMigrationService -ResourceGroupName testResourceGroup
```

<span data-ttu-id="ad7ad-114">В приведенном выше примере выполняется получение служб миграции баз данных Azure в группе ресурсов с именем testResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ad7ad-114">The above example retrieves Azure Database Migration Services in the resource group called testResourceGroup.</span></span> 

## <span data-ttu-id="ad7ad-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ad7ad-115">PARAMETERS</span></span>

### <span data-ttu-id="ad7ad-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad7ad-116">-DefaultProfile</span></span>
<span data-ttu-id="ad7ad-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ad7ad-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad7ad-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ad7ad-118">-Name</span></span>
<span data-ttu-id="ad7ad-119">Имя службы миграции баз данных.</span><span class="sxs-lookup"><span data-stu-id="ad7ad-119">Name of Database Migration Service.</span></span>

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

### <span data-ttu-id="ad7ad-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad7ad-120">-ResourceGroupName</span></span>
<span data-ttu-id="ad7ad-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ad7ad-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="ad7ad-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad7ad-122">-ResourceId</span></span>
<span data-ttu-id="ad7ad-123">Идентификатор ресурса DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="ad7ad-123">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="ad7ad-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad7ad-124">CommonParameters</span></span>
<span data-ttu-id="ad7ad-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ad7ad-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad7ad-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad7ad-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad7ad-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ad7ad-127">INPUTS</span></span>

### <span data-ttu-id="ad7ad-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ad7ad-128">System.String</span></span>

## <span data-ttu-id="ad7ad-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad7ad-129">OUTPUTS</span></span>

### <span data-ttu-id="ad7ad-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="ad7ad-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="ad7ad-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="ad7ad-131">NOTES</span></span>

## <span data-ttu-id="ad7ad-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad7ad-132">RELATED LINKS</span></span>
