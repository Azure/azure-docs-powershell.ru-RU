---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: a3bccd635c5bb2a91cb0b8ea9bc09f93070d447d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560963"
---
# <span data-ttu-id="84bee-101">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="84bee-101">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="84bee-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="84bee-102">SYNOPSIS</span></span>
<span data-ttu-id="84bee-103">Повторное создание ключа среды выполнения интеграции с самостоятельным размещением.</span><span class="sxs-lookup"><span data-stu-id="84bee-103">Regenerate self-hosted integration runtime key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84bee-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="84bee-104">SYNTAX</span></span>

### <span data-ttu-id="84bee-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="84bee-105">ByIntegrationRuntimeName (Default)</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84bee-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="84bee-106">ByResourceId</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84bee-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="84bee-107">ByIntegrationRuntimeObject</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84bee-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="84bee-108">DESCRIPTION</span></span>
<span data-ttu-id="84bee-109">Командлет **New-AzureRmDataFactoryV2IntegrationRuntimeKey** повторно создает ключ среды выполнения Integration с именем ключа, заданным параметром keyName.</span><span class="sxs-lookup"><span data-stu-id="84bee-109">The cmdlet **New-AzureRmDataFactoryV2IntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="84bee-110">Предыдущий ключ не является допустимым.</span><span class="sxs-lookup"><span data-stu-id="84bee-110">The previous key will is invalid.</span></span>

## <span data-ttu-id="84bee-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="84bee-111">EXAMPLES</span></span>

### <span data-ttu-id="84bee-112">Пример 1: создание нового ключа для среды выполнения интеграции</span><span class="sxs-lookup"><span data-stu-id="84bee-112">Example 1: Generate a new key for an integration runtime</span></span>
```
PS C:\> New-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -KeyName authKey2

AuthKey1 AuthKey2
-------- --------
         IR@89895504-f647-48fd-8dd3-42fa556d67e3@***
```

<span data-ttu-id="84bee-113">Командлет повторно создает ключ "authKey2" для среды выполнения интеграции с именем Test-SelfHost-IR.</span><span class="sxs-lookup"><span data-stu-id="84bee-113">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="84bee-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="84bee-114">PARAMETERS</span></span>

### <span data-ttu-id="84bee-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="84bee-115">-DataFactoryName</span></span>
<span data-ttu-id="84bee-116">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="84bee-116">The data factory name.</span></span>

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

### <span data-ttu-id="84bee-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84bee-117">-DefaultProfile</span></span>
<span data-ttu-id="84bee-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="84bee-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84bee-119">-Force</span><span class="sxs-lookup"><span data-stu-id="84bee-119">-Force</span></span>
<span data-ttu-id="84bee-120">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="84bee-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="84bee-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84bee-121">-InputObject</span></span>
<span data-ttu-id="84bee-122">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="84bee-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="84bee-123">-KeyName</span><span class="sxs-lookup"><span data-stu-id="84bee-123">-KeyName</span></span>
<span data-ttu-id="84bee-124">Имя ключа проверки подлинности в среде выполнения интеграции с самостоятельным размещением.</span><span class="sxs-lookup"><span data-stu-id="84bee-124">The authentication key name of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="84bee-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="84bee-125">-Name</span></span>
<span data-ttu-id="84bee-126">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="84bee-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="84bee-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84bee-127">-ResourceGroupName</span></span>
<span data-ttu-id="84bee-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="84bee-128">The resource group name.</span></span>

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

### <span data-ttu-id="84bee-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84bee-129">-ResourceId</span></span>
<span data-ttu-id="84bee-130">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="84bee-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="84bee-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="84bee-131">-Confirm</span></span>
<span data-ttu-id="84bee-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="84bee-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84bee-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84bee-133">-WhatIf</span></span>
<span data-ttu-id="84bee-134">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="84bee-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="84bee-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84bee-135">CommonParameters</span></span>
<span data-ttu-id="84bee-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="84bee-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84bee-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84bee-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84bee-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="84bee-138">INPUTS</span></span>

### <span data-ttu-id="84bee-139">System. String</span><span class="sxs-lookup"><span data-stu-id="84bee-139">System.String</span></span>

### <span data-ttu-id="84bee-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="84bee-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="84bee-141">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="84bee-141">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="84bee-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="84bee-142">OUTPUTS</span></span>

### <span data-ttu-id="84bee-143">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="84bee-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="84bee-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="84bee-144">NOTES</span></span>

## <span data-ttu-id="84bee-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="84bee-145">RELATED LINKS</span></span>

[<span data-ttu-id="84bee-146">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="84bee-146">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()
