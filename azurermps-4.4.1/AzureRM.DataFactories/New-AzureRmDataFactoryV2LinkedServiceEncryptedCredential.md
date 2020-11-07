---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
ms.openlocfilehash: 3face29daf5c6da80e5d6b277850c6639efe96dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732703"
---
# <span data-ttu-id="e90ff-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="e90ff-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="e90ff-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e90ff-102">SYNOPSIS</span></span>
<span data-ttu-id="e90ff-103">Шифрование учетных данных в связанной службе с указанной средой выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="e90ff-103">Encrypt credential in linked service with specified integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e90ff-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e90ff-104">SYNTAX</span></span>

### <span data-ttu-id="e90ff-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e90ff-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e90ff-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e90ff-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e90ff-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e90ff-107">DESCRIPTION</span></span>
<span data-ttu-id="e90ff-108">New-AzureRmDataFactoryV2LinkedServiceEncryptCredential командлетом шифрование учетных данных в связанной службе с указанной средой выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="e90ff-108">The New-AzureRmDataFactoryV2LinkedServiceEncryptCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="e90ff-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e90ff-109">EXAMPLES</span></span>

### <span data-ttu-id="e90ff-110">Пример 1: шифрование creadentials в связанной службе</span><span class="sxs-lookup"><span data-stu-id="e90ff-110">Example 1: Encrypt creadentials in a linked service</span></span>
```
PS C:\> New-AzureRmDataFactoryV2LinkedServiceEncryptCredential -ResourceGroupName resourceGroup -DataFactoryName myDataFactory -IntegrationRuntimeName myIR -File D:\sql.json
```

<span data-ttu-id="e90ff-111">Эта команда шифрует учетные данные в файле D:\sql.jsс помощью среды выполнения интеграции с именем myIR.</span><span class="sxs-lookup"><span data-stu-id="e90ff-111">This command encrypts credential in file D:\sql.json with the integration runtime named myIR.</span></span>

## <span data-ttu-id="e90ff-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e90ff-112">PARAMETERS</span></span>

### <span data-ttu-id="e90ff-113">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="e90ff-113">-DataFactory</span></span>
<span data-ttu-id="e90ff-114">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="e90ff-114">The data factory object.</span></span>

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

### <span data-ttu-id="e90ff-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e90ff-115">-DataFactoryName</span></span>
<span data-ttu-id="e90ff-116">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="e90ff-116">The data factory name.</span></span>

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

### <span data-ttu-id="e90ff-117">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="e90ff-117">-DefinitionFile</span></span>
<span data-ttu-id="e90ff-118">Путь к файлу JSON.</span><span class="sxs-lookup"><span data-stu-id="e90ff-118">The JSON file path.</span></span>

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

### <span data-ttu-id="e90ff-119">-Force</span><span class="sxs-lookup"><span data-stu-id="e90ff-119">-Force</span></span>
<span data-ttu-id="e90ff-120">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="e90ff-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="e90ff-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="e90ff-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="e90ff-122">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="e90ff-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="e90ff-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e90ff-123">-ResourceGroupName</span></span>
<span data-ttu-id="e90ff-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e90ff-124">The resource group name.</span></span>

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

### <span data-ttu-id="e90ff-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e90ff-125">-Confirm</span></span>
<span data-ttu-id="e90ff-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e90ff-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e90ff-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e90ff-127">-WhatIf</span></span>
<span data-ttu-id="e90ff-128">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="e90ff-128">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="e90ff-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e90ff-129">-DefaultProfile</span></span>
<span data-ttu-id="e90ff-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e90ff-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e90ff-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e90ff-131">CommonParameters</span></span>
<span data-ttu-id="e90ff-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e90ff-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e90ff-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e90ff-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e90ff-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e90ff-134">INPUTS</span></span>

### <span data-ttu-id="e90ff-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e90ff-135">System.String</span></span>
<span data-ttu-id="e90ff-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e90ff-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="e90ff-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e90ff-137">OUTPUTS</span></span>

### <span data-ttu-id="e90ff-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e90ff-138">System.String</span></span>

## <span data-ttu-id="e90ff-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="e90ff-139">NOTES</span></span>

## <span data-ttu-id="e90ff-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e90ff-140">RELATED LINKS</span></span>

