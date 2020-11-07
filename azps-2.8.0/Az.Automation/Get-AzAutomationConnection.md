---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D12007E8-8693-45B9-8919-CF8A4BA63AAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
ms.openlocfilehash: 267c18ea4abf87936c47629eca523b254b411240
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727868"
---
# <span data-ttu-id="44a4a-101">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="44a4a-101">Get-AzAutomationConnection</span></span>

## <span data-ttu-id="44a4a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="44a4a-102">SYNOPSIS</span></span>
<span data-ttu-id="44a4a-103">Получает подключение автоматизации.</span><span class="sxs-lookup"><span data-stu-id="44a4a-103">Gets an Automation connection.</span></span>

## <span data-ttu-id="44a4a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="44a4a-104">SYNTAX</span></span>

### <span data-ttu-id="44a4a-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="44a4a-105">ByAll (Default)</span></span>
```
Get-AzAutomationConnection [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44a4a-106">ByConnectionName</span><span class="sxs-lookup"><span data-stu-id="44a4a-106">ByConnectionName</span></span>
```
Get-AzAutomationConnection [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44a4a-107">ByConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="44a4a-107">ByConnectionTypeName</span></span>
```
Get-AzAutomationConnection [-ConnectionTypeName] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44a4a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="44a4a-108">DESCRIPTION</span></span>
<span data-ttu-id="44a4a-109">Командлет **Get-AzAutomationConnection** получает одно или несколько подключений службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="44a4a-109">The **Get-AzAutomationConnection** cmdlet gets one or more Azure Automation connections.</span></span>
<span data-ttu-id="44a4a-110">По умолчанию этот командлет извлекает все подключения.</span><span class="sxs-lookup"><span data-stu-id="44a4a-110">By default, this cmdlet retrieves all connections.</span></span>
<span data-ttu-id="44a4a-111">Укажите имя подключения для получения определенного подключения.</span><span class="sxs-lookup"><span data-stu-id="44a4a-111">Specify the name of a connection to get a specific connection.</span></span>
<span data-ttu-id="44a4a-112">Укажите имя типа подключения, чтобы получить все соединения определенного типа.</span><span class="sxs-lookup"><span data-stu-id="44a4a-112">Specify the connection type name to get all connections of a specific type.</span></span>

## <span data-ttu-id="44a4a-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="44a4a-113">EXAMPLES</span></span>

### <span data-ttu-id="44a4a-114">Пример 1: получение всех подключений</span><span class="sxs-lookup"><span data-stu-id="44a4a-114">Example 1: Get all connections</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="44a4a-115">Эта команда получает метаданные для всех подключений в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="44a4a-115">This command gets metadata for all connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="44a4a-116">Пример 2: получение всех подключений к типу</span><span class="sxs-lookup"><span data-stu-id="44a4a-116">Example 2: Get all connections of a type</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -ConnectionTypeName "SqlServer"
```

<span data-ttu-id="44a4a-117">Эта команда получает метаданные для подключений в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="44a4a-117">This command gets metadata for connections in the Automation account named Contoso17.</span></span>
<span data-ttu-id="44a4a-118">Эта команда получает соединения типа SqlServer.</span><span class="sxs-lookup"><span data-stu-id="44a4a-118">This command gets connections of the type SqlServer.</span></span>

### <span data-ttu-id="44a4a-119">Пример 3: получение подключения</span><span class="sxs-lookup"><span data-stu-id="44a4a-119">Example 3: Get a connection</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoConnection"
```

<span data-ttu-id="44a4a-120">Эта команда получает метаданные для подключения с именем ContosoConnection.</span><span class="sxs-lookup"><span data-stu-id="44a4a-120">This command gets metadata for the connection named ContosoConnection.</span></span>

## <span data-ttu-id="44a4a-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="44a4a-121">PARAMETERS</span></span>

### <span data-ttu-id="44a4a-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="44a4a-122">-AutomationAccountName</span></span>
<span data-ttu-id="44a4a-123">Указывает имя учетной записи автоматизации, для которой этот командлет получает подключения.</span><span class="sxs-lookup"><span data-stu-id="44a4a-123">Specifies the name of the Automation account for which this cmdlet gets connections.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44a4a-124">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="44a4a-124">-ConnectionTypeName</span></span>
<span data-ttu-id="44a4a-125">Указывает имя типа подключения, для которого этот командлет извлекает подключения.</span><span class="sxs-lookup"><span data-stu-id="44a4a-125">Specifies the name of a connection type for which this cmdlet retrieves connections.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConnectionTypeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44a4a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44a4a-126">-DefaultProfile</span></span>
<span data-ttu-id="44a4a-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="44a4a-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="44a4a-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="44a4a-128">-Name</span></span>
<span data-ttu-id="44a4a-129">Указывает имя подключения, которое этот командлет извлекает.</span><span class="sxs-lookup"><span data-stu-id="44a4a-129">Specifies the name of a connection that this cmdlet retrieves.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConnectionName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44a4a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44a4a-130">-ResourceGroupName</span></span>
<span data-ttu-id="44a4a-131">Указывает имя группы ресурсов, для которой этот командлет получает подключения.</span><span class="sxs-lookup"><span data-stu-id="44a4a-131">Specifies the name of a resource group for which this cmdlet gets connections.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44a4a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44a4a-132">CommonParameters</span></span>
<span data-ttu-id="44a4a-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="44a4a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44a4a-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44a4a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44a4a-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="44a4a-135">INPUTS</span></span>

### <span data-ttu-id="44a4a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="44a4a-136">System.String</span></span>

## <span data-ttu-id="44a4a-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="44a4a-137">OUTPUTS</span></span>

### <span data-ttu-id="44a4a-138">Microsoft. Azure. Commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="44a4a-138">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="44a4a-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="44a4a-139">NOTES</span></span>

## <span data-ttu-id="44a4a-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="44a4a-140">RELATED LINKS</span></span>

[<span data-ttu-id="44a4a-141">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="44a4a-141">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)

[<span data-ttu-id="44a4a-142">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="44a4a-142">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


