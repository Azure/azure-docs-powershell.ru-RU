---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 07cb597f5ca3793e3eb8db3fe153fafaa94f3501
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518958"
---
# <span data-ttu-id="23ed2-101">New-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="23ed2-101">New-AzDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="23ed2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23ed2-102">SYNOPSIS</span></span>
<span data-ttu-id="23ed2-103">Повторно сгенерировать ключ времени запуска для самостоятельной интеграции.</span><span class="sxs-lookup"><span data-stu-id="23ed2-103">Regenerate self-hosted integration runtime key.</span></span>

## <span data-ttu-id="23ed2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="23ed2-104">SYNTAX</span></span>

### <span data-ttu-id="23ed2-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="23ed2-105">ByIntegrationRuntimeName (Default)</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23ed2-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="23ed2-106">ByResourceId</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23ed2-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="23ed2-107">ByIntegrationRuntimeObject</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23ed2-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="23ed2-108">DESCRIPTION</span></span>
<span data-ttu-id="23ed2-109">Cmdlet **New-AzDataFactoryV2IntegrationRuntimeKey** повторно сгенерирует ключ времени интеграции с именем ключа, заданным параметром KeyName.</span><span class="sxs-lookup"><span data-stu-id="23ed2-109">The cmdlet **New-AzDataFactoryV2IntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="23ed2-110">Предыдущий ключ недействителен.</span><span class="sxs-lookup"><span data-stu-id="23ed2-110">The previous key will is invalid.</span></span>

## <span data-ttu-id="23ed2-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="23ed2-111">EXAMPLES</span></span>

### <span data-ttu-id="23ed2-112">Пример 1. Создание нового ключа для интегрированного времени запуска</span><span class="sxs-lookup"><span data-stu-id="23ed2-112">Example 1: Generate a new key for an integration runtime</span></span>
```
PS C:\> New-AzDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -KeyName authKey2

AuthKey1 AuthKey2
-------- --------
         IR@89895504-f647-48fd-8dd3-42fa556d67e3@***
```

<span data-ttu-id="23ed2-113">Этот cmdlet повторно сгенерирует ключ authKey2 для интеграции runtime test-selfhost-ir.</span><span class="sxs-lookup"><span data-stu-id="23ed2-113">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="23ed2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23ed2-114">PARAMETERS</span></span>

### <span data-ttu-id="23ed2-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="23ed2-115">-DataFactoryName</span></span>
<span data-ttu-id="23ed2-116">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="23ed2-116">The data factory name.</span></span>

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

### <span data-ttu-id="23ed2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23ed2-117">-DefaultProfile</span></span>
<span data-ttu-id="23ed2-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="23ed2-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23ed2-119">-Force</span><span class="sxs-lookup"><span data-stu-id="23ed2-119">-Force</span></span>
<span data-ttu-id="23ed2-120">Выполняется cmdlet без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="23ed2-120">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23ed2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23ed2-121">-InputObject</span></span>
<span data-ttu-id="23ed2-122">Объект интеграции runtime.</span><span class="sxs-lookup"><span data-stu-id="23ed2-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="23ed2-123">-KeyName</span><span class="sxs-lookup"><span data-stu-id="23ed2-123">-KeyName</span></span>
<span data-ttu-id="23ed2-124">Имя ключа проверки подлинности для самостоятельной интеграции с runtime.</span><span class="sxs-lookup"><span data-stu-id="23ed2-124">The authentication key name of the self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AuthKey1, AuthKey2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23ed2-125">-Name</span><span class="sxs-lookup"><span data-stu-id="23ed2-125">-Name</span></span>
<span data-ttu-id="23ed2-126">Имя времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="23ed2-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="23ed2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23ed2-127">-ResourceGroupName</span></span>
<span data-ttu-id="23ed2-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="23ed2-128">The resource group name.</span></span>

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

### <span data-ttu-id="23ed2-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23ed2-129">-ResourceId</span></span>
<span data-ttu-id="23ed2-130">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="23ed2-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="23ed2-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="23ed2-131">-Confirm</span></span>
<span data-ttu-id="23ed2-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23ed2-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23ed2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23ed2-133">-WhatIf</span></span>
<span data-ttu-id="23ed2-134">Показывает, что происходит, если выполняется только запуск, но не выполняется.</span><span class="sxs-lookup"><span data-stu-id="23ed2-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="23ed2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23ed2-135">CommonParameters</span></span>
<span data-ttu-id="23ed2-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23ed2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23ed2-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23ed2-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23ed2-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="23ed2-138">INPUTS</span></span>

### <span data-ttu-id="23ed2-139">System.String</span><span class="sxs-lookup"><span data-stu-id="23ed2-139">System.String</span></span>

### <span data-ttu-id="23ed2-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="23ed2-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="23ed2-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="23ed2-141">OUTPUTS</span></span>

### <span data-ttu-id="23ed2-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="23ed2-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="23ed2-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="23ed2-143">NOTES</span></span>

## <span data-ttu-id="23ed2-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="23ed2-144">RELATED LINKS</span></span>

[<span data-ttu-id="23ed2-145">Get-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="23ed2-145">Get-AzDataFactoryV2IntegrationRuntimeKey</span></span>]()
