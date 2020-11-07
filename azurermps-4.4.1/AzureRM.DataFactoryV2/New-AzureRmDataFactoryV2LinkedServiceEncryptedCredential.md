---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 9960a34d19c4016461ddfc53a37f83d3e73e7526
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734072"
---
# <span data-ttu-id="d66f5-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="d66f5-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="d66f5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d66f5-102">SYNOPSIS</span></span>
<span data-ttu-id="d66f5-103">Шифрование учетных данных в связанной службе с указанной средой выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="d66f5-103">Encrypt credential in linked service with specified integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d66f5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d66f5-104">SYNTAX</span></span>

### <span data-ttu-id="d66f5-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d66f5-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="d66f5-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d66f5-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="d66f5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d66f5-107">DESCRIPTION</span></span>
<span data-ttu-id="d66f5-108">New-AzureRmDataFactoryV2LinkedServiceEncryptCredential командлетом шифрование учетных данных в связанной службе с указанной средой выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="d66f5-108">The New-AzureRmDataFactoryV2LinkedServiceEncryptCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="d66f5-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d66f5-109">EXAMPLES</span></span>

### <span data-ttu-id="d66f5-110">Пример 1: шифрование creadentials в связанной службе</span><span class="sxs-lookup"><span data-stu-id="d66f5-110">Example 1: Encrypt creadentials in a linked service</span></span>
```
PS C:\> New-AzureRmDataFactoryV2LinkedServiceEncryptCredential -ResourceGroupName resourceGroup -DataFactoryName myDataFactory -IntegrationRuntimeName myIR -File D:\sql.json
```

<span data-ttu-id="d66f5-111">Эта команда шифрует учетные данные в файле D:\sql.jsс помощью среды выполнения интеграции с именем myIR.</span><span class="sxs-lookup"><span data-stu-id="d66f5-111">This command encrypts credential in file D:\sql.json with the integration runtime named myIR.</span></span>

## <span data-ttu-id="d66f5-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d66f5-112">PARAMETERS</span></span>

### <span data-ttu-id="d66f5-113">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="d66f5-113">-DataFactory</span></span>
<span data-ttu-id="d66f5-114">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="d66f5-114">The data factory object.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d66f5-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d66f5-115">-DataFactoryName</span></span>
<span data-ttu-id="d66f5-116">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="d66f5-116">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d66f5-117">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="d66f5-117">-DefinitionFile</span></span>
<span data-ttu-id="d66f5-118">Путь к файлу JSON.</span><span class="sxs-lookup"><span data-stu-id="d66f5-118">The JSON file path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d66f5-119">-Force</span><span class="sxs-lookup"><span data-stu-id="d66f5-119">-Force</span></span>
<span data-ttu-id="d66f5-120">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="d66f5-120">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d66f5-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="d66f5-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="d66f5-122">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="d66f5-122">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d66f5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d66f5-123">-ResourceGroupName</span></span>
<span data-ttu-id="d66f5-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d66f5-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d66f5-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d66f5-125">-Confirm</span></span>
<span data-ttu-id="d66f5-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d66f5-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d66f5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d66f5-127">-WhatIf</span></span>
<span data-ttu-id="d66f5-128">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="d66f5-128">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="d66f5-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d66f5-129">INPUTS</span></span>

### <span data-ttu-id="d66f5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d66f5-130">System.String</span></span>
<span data-ttu-id="d66f5-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d66f5-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="d66f5-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d66f5-132">OUTPUTS</span></span>

### <span data-ttu-id="d66f5-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d66f5-133">System.String</span></span>


## <span data-ttu-id="d66f5-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="d66f5-134">NOTES</span></span>

## <span data-ttu-id="d66f5-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d66f5-135">RELATED LINKS</span></span>

