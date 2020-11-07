---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryv2linkedserviceencryptedcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
ms.openlocfilehash: bdc3d9b997a98ca67c2848ada32d8fc94fa20e09
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721488"
---
# <span data-ttu-id="04866-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="04866-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="04866-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="04866-102">SYNOPSIS</span></span>
<span data-ttu-id="04866-103">Шифрование учетных данных в связанной службе с указанной средой выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="04866-103">Encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="04866-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="04866-104">SYNTAX</span></span>

### <span data-ttu-id="04866-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="04866-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04866-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="04866-106">ByFactoryObject</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04866-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="04866-107">DESCRIPTION</span></span>
<span data-ttu-id="04866-108">New-AzDataFactoryV2LinkedServiceEncryptCredential командлетом шифрование учетных данных в связанной службе с указанной средой выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="04866-108">The New-AzDataFactoryV2LinkedServiceEncryptCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="04866-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="04866-109">EXAMPLES</span></span>

### <span data-ttu-id="04866-110">Пример 1: Шифрование учетных данных в связанной службе</span><span class="sxs-lookup"><span data-stu-id="04866-110">Example 1: Encrypt credentials in a linked service</span></span>
```
PS C:\> New-AzDataFactoryV2LinkedServiceEncryptCredential -ResourceGroupName resourceGroup -DataFactoryName myDataFactory -IntegrationRuntimeName myIR -File D:\sql.json
```

<span data-ttu-id="04866-111">Эта команда шифрует учетные данные в файле D:\sql.jsс помощью среды выполнения интеграции с именем myIR.</span><span class="sxs-lookup"><span data-stu-id="04866-111">This command encrypts credential in file D:\sql.json with the integration runtime named myIR.</span></span>

## <span data-ttu-id="04866-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="04866-112">PARAMETERS</span></span>

### <span data-ttu-id="04866-113">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="04866-113">-DataFactory</span></span>
<span data-ttu-id="04866-114">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="04866-114">The data factory object.</span></span>

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

### <span data-ttu-id="04866-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="04866-115">-DataFactoryName</span></span>
<span data-ttu-id="04866-116">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="04866-116">The data factory name.</span></span>

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

### <span data-ttu-id="04866-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04866-117">-DefaultProfile</span></span>
<span data-ttu-id="04866-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="04866-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04866-119">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="04866-119">-DefinitionFile</span></span>
<span data-ttu-id="04866-120">Путь к файлу JSON.</span><span class="sxs-lookup"><span data-stu-id="04866-120">The JSON file path.</span></span>

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

### <span data-ttu-id="04866-121">-Force</span><span class="sxs-lookup"><span data-stu-id="04866-121">-Force</span></span>
<span data-ttu-id="04866-122">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="04866-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="04866-123">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="04866-123">-IntegrationRuntimeName</span></span>
<span data-ttu-id="04866-124">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="04866-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="04866-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04866-125">-ResourceGroupName</span></span>
<span data-ttu-id="04866-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="04866-126">The resource group name.</span></span>

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

### <span data-ttu-id="04866-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="04866-127">-Confirm</span></span>
<span data-ttu-id="04866-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="04866-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04866-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04866-129">-WhatIf</span></span>
<span data-ttu-id="04866-130">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="04866-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="04866-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04866-131">CommonParameters</span></span>
<span data-ttu-id="04866-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="04866-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04866-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04866-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04866-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="04866-134">INPUTS</span></span>

### <span data-ttu-id="04866-135">System. String</span><span class="sxs-lookup"><span data-stu-id="04866-135">System.String</span></span>

### <span data-ttu-id="04866-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="04866-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="04866-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="04866-137">OUTPUTS</span></span>

### <span data-ttu-id="04866-138">System. String</span><span class="sxs-lookup"><span data-stu-id="04866-138">System.String</span></span>

## <span data-ttu-id="04866-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="04866-139">NOTES</span></span>

## <span data-ttu-id="04866-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="04866-140">RELATED LINKS</span></span>
