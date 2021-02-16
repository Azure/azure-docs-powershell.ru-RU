---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryv2linkedserviceencryptedcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
ms.openlocfilehash: a99f7fbb1383d685a53cc11f9dd81f6f306ed633
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242789"
---
# <span data-ttu-id="ffcba-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="ffcba-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="ffcba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffcba-102">SYNOPSIS</span></span>
<span data-ttu-id="ffcba-103">Зашифровать учетные данные в связанной службе, заданную временную ацию интеграции.</span><span class="sxs-lookup"><span data-stu-id="ffcba-103">Encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="ffcba-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ffcba-104">SYNTAX</span></span>

### <span data-ttu-id="ffcba-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ffcba-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffcba-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ffcba-106">ByFactoryObject</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffcba-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ffcba-107">DESCRIPTION</span></span>
<span data-ttu-id="ffcba-108">Учетные New-AzDataFactoryV2LinkedServiceEncryptedCredential шифруются в связанной службе с указанной временем интеграции.</span><span class="sxs-lookup"><span data-stu-id="ffcba-108">The New-AzDataFactoryV2LinkedServiceEncryptedCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

<span data-ttu-id="ffcba-109">Убедитесь, что выполнены следующие необходимые условия:</span><span class="sxs-lookup"><span data-stu-id="ffcba-109">Please ensure the following prerequisites are met:</span></span>
* <span data-ttu-id="ffcba-110">**Параметр удаленного** доступа включен в режиме самостоятельной интеграции.</span><span class="sxs-lookup"><span data-stu-id="ffcba-110">**Remote access** option is enabled on the self-hosted integration runtime.</span></span>
* <span data-ttu-id="ffcba-111">Для выполнения cmdlet используется powershell 7.0 или более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="ffcba-111">Powershell 7.0 or higher is used to execute the cmdlet.</span></span>

## <span data-ttu-id="ffcba-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ffcba-112">EXAMPLES</span></span>

### <span data-ttu-id="ffcba-113">Пример 1. Шифрование учетных данных в связанной службе</span><span class="sxs-lookup"><span data-stu-id="ffcba-113">Example 1: Encrypt credentials in a linked service</span></span>

<span data-ttu-id="ffcba-114">Эта команда шифрует учетные данные в C:\samples\WikiSample\TaxiDemo1.jsс помощью интеграции runtime test-selfhost-ir.</span><span class="sxs-lookup"><span data-stu-id="ffcba-114">This command encrypts credential in file C:\samples\WikiSample\TaxiDemo1.json with the integration runtime named test-selfhost-ir.</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzDataFactoryV2LinkedServiceEncryptedCredential -DataFactoryName WikiADF -DefinitionFile 'C:\samples\WikiSample\TaxiDemo1.json' -IntegrationRuntimeName 'test-selfhost-ir' -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="ffcba-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ffcba-115">PARAMETERS</span></span>

### <span data-ttu-id="ffcba-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="ffcba-116">-DataFactory</span></span>
<span data-ttu-id="ffcba-117">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="ffcba-117">The data factory object.</span></span>

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

### <span data-ttu-id="ffcba-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ffcba-118">-DataFactoryName</span></span>
<span data-ttu-id="ffcba-119">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="ffcba-119">The data factory name.</span></span>

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

### <span data-ttu-id="ffcba-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffcba-120">-DefaultProfile</span></span>
<span data-ttu-id="ffcba-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ffcba-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ffcba-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="ffcba-122">-DefinitionFile</span></span>
<span data-ttu-id="ffcba-123">Путь к файлу JSON.</span><span class="sxs-lookup"><span data-stu-id="ffcba-123">The JSON file path.</span></span>

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

### <span data-ttu-id="ffcba-124">-Force</span><span class="sxs-lookup"><span data-stu-id="ffcba-124">-Force</span></span>
<span data-ttu-id="ffcba-125">Выполняется cmdlet без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="ffcba-125">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ffcba-126">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="ffcba-126">-IntegrationRuntimeName</span></span>
<span data-ttu-id="ffcba-127">Имя времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="ffcba-127">The integration runtime name.</span></span>

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

### <span data-ttu-id="ffcba-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffcba-128">-ResourceGroupName</span></span>
<span data-ttu-id="ffcba-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ffcba-129">The resource group name.</span></span>

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

### <span data-ttu-id="ffcba-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ffcba-130">-Confirm</span></span>
<span data-ttu-id="ffcba-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ffcba-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffcba-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffcba-132">-WhatIf</span></span>
<span data-ttu-id="ffcba-133">Показывает, что происходит, если выполняется только запуск, но не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ffcba-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="ffcba-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffcba-134">CommonParameters</span></span>
<span data-ttu-id="ffcba-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffcba-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffcba-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffcba-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffcba-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ffcba-137">INPUTS</span></span>

### <span data-ttu-id="ffcba-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ffcba-138">System.String</span></span>

### <span data-ttu-id="ffcba-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ffcba-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="ffcba-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ffcba-140">OUTPUTS</span></span>

### <span data-ttu-id="ffcba-141">System.String</span><span class="sxs-lookup"><span data-stu-id="ffcba-141">System.String</span></span>

## <span data-ttu-id="ffcba-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ffcba-142">NOTES</span></span>

## <span data-ttu-id="ffcba-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ffcba-143">RELATED LINKS</span></span>
