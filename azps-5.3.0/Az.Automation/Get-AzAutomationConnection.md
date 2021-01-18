---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D12007E8-8693-45B9-8919-CF8A4BA63AAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
ms.openlocfilehash: 3cf369be5c7d62d9e4b85002906d55f34a47e40c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98510125"
---
# <span data-ttu-id="5c0cd-101">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="5c0cd-101">Get-AzAutomationConnection</span></span>

## <span data-ttu-id="5c0cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c0cd-102">SYNOPSIS</span></span>
<span data-ttu-id="5c0cd-103">Подключение автоматизации.</span><span class="sxs-lookup"><span data-stu-id="5c0cd-103">Gets an Automation connection.</span></span>

## <span data-ttu-id="5c0cd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5c0cd-104">SYNTAX</span></span>

### <span data-ttu-id="5c0cd-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5c0cd-105">ByAll (Default)</span></span>
```
Get-AzAutomationConnection [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c0cd-106">ByConnectionName</span><span class="sxs-lookup"><span data-stu-id="5c0cd-106">ByConnectionName</span></span>
```
Get-AzAutomationConnection [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c0cd-107">ByConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="5c0cd-107">ByConnectionTypeName</span></span>
```
Get-AzAutomationConnection [-ConnectionTypeName] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c0cd-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c0cd-108">DESCRIPTION</span></span>
<span data-ttu-id="5c0cd-109">Для **этого требуется одно или** несколько подключений автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="5c0cd-109">The **Get-AzAutomationConnection** cmdlet gets one or more Azure Automation connections.</span></span>
<span data-ttu-id="5c0cd-110">По умолчанию этот cmdlet извлекает все подключения.</span><span class="sxs-lookup"><span data-stu-id="5c0cd-110">By default, this cmdlet retrieves all connections.</span></span>
<span data-ttu-id="5c0cd-111">Укажите имя подключения, чтобы получить определенное подключение.</span><span class="sxs-lookup"><span data-stu-id="5c0cd-111">Specify the name of a connection to get a specific connection.</span></span>
<span data-ttu-id="5c0cd-112">Укажите имя типа подключения, чтобы получить все подключения определенного типа.</span><span class="sxs-lookup"><span data-stu-id="5c0cd-112">Specify the connection type name to get all connections of a specific type.</span></span>

## <span data-ttu-id="5c0cd-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5c0cd-113">EXAMPLES</span></span>

### <span data-ttu-id="5c0cd-114">Пример 1. Получить все подключения</span><span class="sxs-lookup"><span data-stu-id="5c0cd-114">Example 1: Get all connections</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="5c0cd-115">Эта команда получает метаданные для всех подключений в учетной записи автоматизации Contoso17.</span><span class="sxs-lookup"><span data-stu-id="5c0cd-115">This command gets metadata for all connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="5c0cd-116">Пример 2. Получить все подключения одного типа</span><span class="sxs-lookup"><span data-stu-id="5c0cd-116">Example 2: Get all connections of a type</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -ConnectionTypeName "SqlServer"
```

<span data-ttu-id="5c0cd-117">Эта команда получает метаданные для подключений в учетной записи автоматизации Contoso17.</span><span class="sxs-lookup"><span data-stu-id="5c0cd-117">This command gets metadata for connections in the Automation account named Contoso17.</span></span>
<span data-ttu-id="5c0cd-118">Эта команда получает соединения типа SqlServer.</span><span class="sxs-lookup"><span data-stu-id="5c0cd-118">This command gets connections of the type SqlServer.</span></span>

### <span data-ttu-id="5c0cd-119">Пример 3. Подключение</span><span class="sxs-lookup"><span data-stu-id="5c0cd-119">Example 3: Get a connection</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoConnection"
```

<span data-ttu-id="5c0cd-120">Эта команда получает метаданные подключения ContosoConnection.</span><span class="sxs-lookup"><span data-stu-id="5c0cd-120">This command gets metadata for the connection named ContosoConnection.</span></span>

## <span data-ttu-id="5c0cd-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c0cd-121">PARAMETERS</span></span>

### <span data-ttu-id="5c0cd-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5c0cd-122">-AutomationAccountName</span></span>
<span data-ttu-id="5c0cd-123">Указывает имя учетной записи автоматизации, для которой этот cmdlet получает подключения.</span><span class="sxs-lookup"><span data-stu-id="5c0cd-123">Specifies the name of the Automation account for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="5c0cd-124">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="5c0cd-124">-ConnectionTypeName</span></span>
<span data-ttu-id="5c0cd-125">Указывает имя типа подключения, для которого этот cmdlet извлекает соединения.</span><span class="sxs-lookup"><span data-stu-id="5c0cd-125">Specifies the name of a connection type for which this cmdlet retrieves connections.</span></span>

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

### <span data-ttu-id="5c0cd-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c0cd-126">-DefaultProfile</span></span>
<span data-ttu-id="5c0cd-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5c0cd-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c0cd-128">-Name</span><span class="sxs-lookup"><span data-stu-id="5c0cd-128">-Name</span></span>
<span data-ttu-id="5c0cd-129">Указывает имя подключения, которое извлекает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c0cd-129">Specifies the name of a connection that this cmdlet retrieves.</span></span>

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

### <span data-ttu-id="5c0cd-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c0cd-130">-ResourceGroupName</span></span>
<span data-ttu-id="5c0cd-131">Имя группы ресурсов, для которой этот cmdlet получает подключения.</span><span class="sxs-lookup"><span data-stu-id="5c0cd-131">Specifies the name of a resource group for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="5c0cd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c0cd-132">CommonParameters</span></span>
<span data-ttu-id="5c0cd-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c0cd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c0cd-134">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c0cd-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c0cd-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5c0cd-135">INPUTS</span></span>

### <span data-ttu-id="5c0cd-136">System.String</span><span class="sxs-lookup"><span data-stu-id="5c0cd-136">System.String</span></span>

## <span data-ttu-id="5c0cd-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5c0cd-137">OUTPUTS</span></span>

### <span data-ttu-id="5c0cd-138">Microsoft.Azure.Commands.Automation.Model.Connection</span><span class="sxs-lookup"><span data-stu-id="5c0cd-138">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="5c0cd-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5c0cd-139">NOTES</span></span>

## <span data-ttu-id="5c0cd-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5c0cd-140">RELATED LINKS</span></span>

[<span data-ttu-id="5c0cd-141">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="5c0cd-141">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)

[<span data-ttu-id="5c0cd-142">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="5c0cd-142">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


