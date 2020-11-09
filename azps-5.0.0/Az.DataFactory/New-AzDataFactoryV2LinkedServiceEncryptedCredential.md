---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryv2linkedserviceencryptedcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
ms.openlocfilehash: 0ff9ef1337a1f2a5f0503c59dc4e6240d3c959b4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313907"
---
# <span data-ttu-id="e88a4-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="e88a4-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="e88a4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e88a4-102">SYNOPSIS</span></span>
<span data-ttu-id="e88a4-103">Шифрование учетных данных в связанной службе с указанной средой выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="e88a4-103">Encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="e88a4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e88a4-104">SYNTAX</span></span>

### <span data-ttu-id="e88a4-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e88a4-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e88a4-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e88a4-106">ByFactoryObject</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e88a4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e88a4-107">DESCRIPTION</span></span>
<span data-ttu-id="e88a4-108">New-AzDataFactoryV2LinkedServiceEncryptedCredential командлетом шифрование учетных данных в связанной службе с указанной средой выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="e88a4-108">The New-AzDataFactoryV2LinkedServiceEncryptedCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="e88a4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e88a4-109">EXAMPLES</span></span>

### <span data-ttu-id="e88a4-110">Пример 1: Шифрование учетных данных в связанной службе</span><span class="sxs-lookup"><span data-stu-id="e88a4-110">Example 1: Encrypt credentials in a linked service</span></span>

<span data-ttu-id="e88a4-111">Эта команда шифрует учетные данные в файле C:\samples\WikiSample\TaxiDemo1.jsс помощью среды выполнения интеграции с именем Test-SelfHost-IR.</span><span class="sxs-lookup"><span data-stu-id="e88a4-111">This command encrypts credential in file C:\samples\WikiSample\TaxiDemo1.json with the integration runtime named test-selfhost-ir.</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzDataFactoryV2LinkedServiceEncryptedCredential -DataFactoryName WikiADF -DefinitionFile 'C:\samples\WikiSample\TaxiDemo1.json' -IntegrationRuntimeName 'test-selfhost-ir' -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="e88a4-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e88a4-112">PARAMETERS</span></span>

### <span data-ttu-id="e88a4-113">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="e88a4-113">-DataFactory</span></span>
<span data-ttu-id="e88a4-114">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="e88a4-114">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e88a4-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e88a4-115">-DataFactoryName</span></span>
<span data-ttu-id="e88a4-116">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="e88a4-116">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e88a4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e88a4-117">-DefaultProfile</span></span>
<span data-ttu-id="e88a4-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e88a4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e88a4-119">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="e88a4-119">-DefinitionFile</span></span>
<span data-ttu-id="e88a4-120">Путь к файлу JSON.</span><span class="sxs-lookup"><span data-stu-id="e88a4-120">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e88a4-121">-Force</span><span class="sxs-lookup"><span data-stu-id="e88a4-121">-Force</span></span>
<span data-ttu-id="e88a4-122">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="e88a4-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="e88a4-123">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="e88a4-123">-IntegrationRuntimeName</span></span>
<span data-ttu-id="e88a4-124">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="e88a4-124">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e88a4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e88a4-125">-ResourceGroupName</span></span>
<span data-ttu-id="e88a4-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e88a4-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e88a4-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e88a4-127">-Confirm</span></span>
<span data-ttu-id="e88a4-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e88a4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e88a4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e88a4-129">-WhatIf</span></span>
<span data-ttu-id="e88a4-130">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="e88a4-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="e88a4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e88a4-131">CommonParameters</span></span>
<span data-ttu-id="e88a4-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e88a4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e88a4-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e88a4-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e88a4-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e88a4-134">INPUTS</span></span>

### <span data-ttu-id="e88a4-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e88a4-135">System.String</span></span>

### <span data-ttu-id="e88a4-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e88a4-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="e88a4-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e88a4-137">OUTPUTS</span></span>

### <span data-ttu-id="e88a4-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e88a4-138">System.String</span></span>

## <span data-ttu-id="e88a4-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="e88a4-139">NOTES</span></span>

## <span data-ttu-id="e88a4-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e88a4-140">RELATED LINKS</span></span>
