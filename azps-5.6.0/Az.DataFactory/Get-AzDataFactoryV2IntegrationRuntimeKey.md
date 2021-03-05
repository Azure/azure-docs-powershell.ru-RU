---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: fc47b71b1546fe351f9d535da4ef9942af66f19e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975256"
---
# <span data-ttu-id="2f112-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="2f112-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="2f112-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f112-102">SYNOPSIS</span></span>
<span data-ttu-id="2f112-103">Ключи для самостоятельной интеграции во время работы.</span><span class="sxs-lookup"><span data-stu-id="2f112-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="2f112-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2f112-104">SYNTAX</span></span>

### <span data-ttu-id="2f112-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2f112-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f112-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2f112-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2f112-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="2f112-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f112-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f112-108">DESCRIPTION</span></span>
<span data-ttu-id="2f112-109">Получите ключи для интеграции с runtime.</span><span class="sxs-lookup"><span data-stu-id="2f112-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="2f112-110">Ключи используются для регистрации узла интеграции runtime.</span><span class="sxs-lookup"><span data-stu-id="2f112-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="2f112-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2f112-111">EXAMPLES</span></span>

### <span data-ttu-id="2f112-112">Пример 1. Получите ключи времени интеграции со временем запуска</span><span class="sxs-lookup"><span data-stu-id="2f112-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="2f112-113">Он извлекает ключи для интеграции с именем test-selfhost-ir.</span><span class="sxs-lookup"><span data-stu-id="2f112-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="2f112-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f112-114">PARAMETERS</span></span>

### <span data-ttu-id="2f112-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2f112-115">-DataFactoryName</span></span>
<span data-ttu-id="2f112-116">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="2f112-116">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f112-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f112-117">-DefaultProfile</span></span>
<span data-ttu-id="2f112-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2f112-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f112-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f112-119">-InputObject</span></span>
<span data-ttu-id="2f112-120">Объект runtime интеграции.</span><span class="sxs-lookup"><span data-stu-id="2f112-120">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f112-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2f112-121">-Name</span></span>
<span data-ttu-id="2f112-122">Имя времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="2f112-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f112-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f112-123">-ResourceGroupName</span></span>
<span data-ttu-id="2f112-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2f112-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f112-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f112-125">-ResourceId</span></span>
<span data-ttu-id="2f112-126">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="2f112-126">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f112-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f112-127">CommonParameters</span></span>
<span data-ttu-id="2f112-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f112-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f112-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f112-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f112-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2f112-130">INPUTS</span></span>

### <span data-ttu-id="2f112-131">System.String</span><span class="sxs-lookup"><span data-stu-id="2f112-131">System.String</span></span>

### <span data-ttu-id="2f112-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2f112-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="2f112-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2f112-133">OUTPUTS</span></span>

### <span data-ttu-id="2f112-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="2f112-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="2f112-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2f112-135">NOTES</span></span>

## <span data-ttu-id="2f112-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2f112-136">RELATED LINKS</span></span>

[<span data-ttu-id="2f112-137">New-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="2f112-137">New-AzDataFactoryV2IntegrationRuntimeKey</span></span>]()
