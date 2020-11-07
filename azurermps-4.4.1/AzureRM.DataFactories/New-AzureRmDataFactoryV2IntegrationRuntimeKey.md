---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: becbcd3e7bbc0a86a2b092921fd5060dd56e927b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734877"
---
# <span data-ttu-id="66b4c-101">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="66b4c-101">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="66b4c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="66b4c-102">SYNOPSIS</span></span>
<span data-ttu-id="66b4c-103">Повторное создание ключа среды выполнения интеграции с самостоятельным размещением.</span><span class="sxs-lookup"><span data-stu-id="66b4c-103">Regenerate self-hosted integration runtime key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66b4c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="66b4c-104">SYNTAX</span></span>

### <span data-ttu-id="66b4c-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="66b4c-105">ByIntegrationRuntimeName (Default)</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66b4c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="66b4c-106">ByResourceId</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66b4c-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="66b4c-107">ByIntegrationRuntimeObject</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66b4c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="66b4c-108">DESCRIPTION</span></span>
<span data-ttu-id="66b4c-109">Командлет **New-AzureRmDataFactoryV2IntegrationRuntimeKey** повторно создает ключ среды выполнения Integration с именем ключа, заданным параметром keyName.</span><span class="sxs-lookup"><span data-stu-id="66b4c-109">The cmdlet **New-AzureRmDataFactoryV2IntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="66b4c-110">Предыдущий ключ не является допустимым.</span><span class="sxs-lookup"><span data-stu-id="66b4c-110">The previous key will is invalid.</span></span>

## <span data-ttu-id="66b4c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="66b4c-111">EXAMPLES</span></span>

### <span data-ttu-id="66b4c-112">Пример 1: создание нового ключа для среды выполнения интеграции</span><span class="sxs-lookup"><span data-stu-id="66b4c-112">Example 1: Generate a new key for an integration runtime</span></span>
```
PS C:\> New-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -KeyName authKey2

AuthKey1 AuthKey2
-------- --------
         IR@89895504-f647-48fd-8dd3-42fa556d67e3@***
```

<span data-ttu-id="66b4c-113">Командлет повторно создает ключ "authKey2" для среды выполнения интеграции с именем Test-SelfHost-IR.</span><span class="sxs-lookup"><span data-stu-id="66b4c-113">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="66b4c-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="66b4c-114">PARAMETERS</span></span>

### <span data-ttu-id="66b4c-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="66b4c-115">-Confirm</span></span>
<span data-ttu-id="66b4c-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="66b4c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66b4c-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="66b4c-117">-DataFactoryName</span></span>
<span data-ttu-id="66b4c-118">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="66b4c-118">The data factory name.</span></span>

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

### <span data-ttu-id="66b4c-119">-Force</span><span class="sxs-lookup"><span data-stu-id="66b4c-119">-Force</span></span>
<span data-ttu-id="66b4c-120">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="66b4c-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="66b4c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66b4c-121">-InputObject</span></span>
<span data-ttu-id="66b4c-122">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="66b4c-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="66b4c-123">-KeyName</span><span class="sxs-lookup"><span data-stu-id="66b4c-123">-KeyName</span></span>
<span data-ttu-id="66b4c-124">Имя ключа проверки подлинности в среде выполнения интеграции с самостоятельным размещением.</span><span class="sxs-lookup"><span data-stu-id="66b4c-124">The authentication key name of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="66b4c-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="66b4c-125">-Name</span></span>
<span data-ttu-id="66b4c-126">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="66b4c-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="66b4c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66b4c-127">-ResourceGroupName</span></span>
<span data-ttu-id="66b4c-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="66b4c-128">The resource group name.</span></span>

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

### <span data-ttu-id="66b4c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66b4c-129">-ResourceId</span></span>
<span data-ttu-id="66b4c-130">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="66b4c-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="66b4c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66b4c-131">-WhatIf</span></span>
<span data-ttu-id="66b4c-132">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="66b4c-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="66b4c-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66b4c-133">-DefaultProfile</span></span>
<span data-ttu-id="66b4c-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="66b4c-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66b4c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66b4c-135">CommonParameters</span></span>
<span data-ttu-id="66b4c-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="66b4c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66b4c-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66b4c-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66b4c-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="66b4c-138">INPUTS</span></span>

### <span data-ttu-id="66b4c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="66b4c-139">System.String</span></span>
<span data-ttu-id="66b4c-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="66b4c-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="66b4c-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="66b4c-141">OUTPUTS</span></span>

### <span data-ttu-id="66b4c-142">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="66b4c-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="66b4c-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="66b4c-143">NOTES</span></span>

## <span data-ttu-id="66b4c-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="66b4c-144">RELATED LINKS</span></span>

[<span data-ttu-id="66b4c-145">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="66b4c-145">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()
