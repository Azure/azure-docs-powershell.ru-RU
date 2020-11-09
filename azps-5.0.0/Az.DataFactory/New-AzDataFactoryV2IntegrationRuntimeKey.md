---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 07cb597f5ca3793e3eb8db3fe153fafaa94f3501
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313904"
---
# <span data-ttu-id="78539-101">New-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="78539-101">New-AzDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="78539-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="78539-102">SYNOPSIS</span></span>
<span data-ttu-id="78539-103">Повторное создание ключа среды выполнения интеграции с самостоятельным размещением.</span><span class="sxs-lookup"><span data-stu-id="78539-103">Regenerate self-hosted integration runtime key.</span></span>

## <span data-ttu-id="78539-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="78539-104">SYNTAX</span></span>

### <span data-ttu-id="78539-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="78539-105">ByIntegrationRuntimeName (Default)</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78539-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="78539-106">ByResourceId</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78539-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="78539-107">ByIntegrationRuntimeObject</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78539-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="78539-108">DESCRIPTION</span></span>
<span data-ttu-id="78539-109">Командлет **New-AzDataFactoryV2IntegrationRuntimeKey** повторно создает ключ среды выполнения Integration с именем ключа, заданным параметром keyName.</span><span class="sxs-lookup"><span data-stu-id="78539-109">The cmdlet **New-AzDataFactoryV2IntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="78539-110">Предыдущий ключ не является допустимым.</span><span class="sxs-lookup"><span data-stu-id="78539-110">The previous key will is invalid.</span></span>

## <span data-ttu-id="78539-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="78539-111">EXAMPLES</span></span>

### <span data-ttu-id="78539-112">Пример 1: создание нового ключа для среды выполнения интеграции</span><span class="sxs-lookup"><span data-stu-id="78539-112">Example 1: Generate a new key for an integration runtime</span></span>
```
PS C:\> New-AzDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -KeyName authKey2

AuthKey1 AuthKey2
-------- --------
         IR@89895504-f647-48fd-8dd3-42fa556d67e3@***
```

<span data-ttu-id="78539-113">Командлет повторно создает ключ "authKey2" для среды выполнения интеграции с именем Test-SelfHost-IR.</span><span class="sxs-lookup"><span data-stu-id="78539-113">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="78539-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="78539-114">PARAMETERS</span></span>

### <span data-ttu-id="78539-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="78539-115">-DataFactoryName</span></span>
<span data-ttu-id="78539-116">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="78539-116">The data factory name.</span></span>

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

### <span data-ttu-id="78539-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78539-117">-DefaultProfile</span></span>
<span data-ttu-id="78539-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="78539-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78539-119">-Force</span><span class="sxs-lookup"><span data-stu-id="78539-119">-Force</span></span>
<span data-ttu-id="78539-120">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="78539-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="78539-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78539-121">-InputObject</span></span>
<span data-ttu-id="78539-122">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="78539-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="78539-123">-KeyName</span><span class="sxs-lookup"><span data-stu-id="78539-123">-KeyName</span></span>
<span data-ttu-id="78539-124">Имя ключа проверки подлинности в среде выполнения интеграции с самостоятельным размещением.</span><span class="sxs-lookup"><span data-stu-id="78539-124">The authentication key name of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="78539-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="78539-125">-Name</span></span>
<span data-ttu-id="78539-126">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="78539-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="78539-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78539-127">-ResourceGroupName</span></span>
<span data-ttu-id="78539-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="78539-128">The resource group name.</span></span>

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

### <span data-ttu-id="78539-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78539-129">-ResourceId</span></span>
<span data-ttu-id="78539-130">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="78539-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="78539-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="78539-131">-Confirm</span></span>
<span data-ttu-id="78539-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="78539-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78539-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78539-133">-WhatIf</span></span>
<span data-ttu-id="78539-134">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="78539-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="78539-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78539-135">CommonParameters</span></span>
<span data-ttu-id="78539-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="78539-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78539-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78539-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78539-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="78539-138">INPUTS</span></span>

### <span data-ttu-id="78539-139">System. String</span><span class="sxs-lookup"><span data-stu-id="78539-139">System.String</span></span>

### <span data-ttu-id="78539-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="78539-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="78539-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="78539-141">OUTPUTS</span></span>

### <span data-ttu-id="78539-142">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="78539-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="78539-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="78539-143">NOTES</span></span>

## <span data-ttu-id="78539-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="78539-144">RELATED LINKS</span></span>

[<span data-ttu-id="78539-145">Get-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="78539-145">Get-AzDataFactoryV2IntegrationRuntimeKey</span></span>]()
