---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D12007E8-8693-45B9-8919-CF8A4BA63AAA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationConnection.md
ms.openlocfilehash: e83a4c71656feb9dbe766339244e54038fa56c84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567192"
---
# <span data-ttu-id="7434a-101">Get-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="7434a-101">Get-AzureRmAutomationConnection</span></span>

## <span data-ttu-id="7434a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7434a-102">SYNOPSIS</span></span>
<span data-ttu-id="7434a-103">Получает подключение автоматизации.</span><span class="sxs-lookup"><span data-stu-id="7434a-103">Gets an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7434a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7434a-104">SYNTAX</span></span>

### <span data-ttu-id="7434a-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7434a-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationConnection [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7434a-106">ByConnectionName</span><span class="sxs-lookup"><span data-stu-id="7434a-106">ByConnectionName</span></span>
```
Get-AzureRmAutomationConnection [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7434a-107">ByConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="7434a-107">ByConnectionTypeName</span></span>
```
Get-AzureRmAutomationConnection [-ConnectionTypeName] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7434a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7434a-108">DESCRIPTION</span></span>
<span data-ttu-id="7434a-109">Командлет **Get-AzureRmAutomationConnection** получает одно или несколько подключений службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="7434a-109">The **Get-AzureRmAutomationConnection** cmdlet gets one or more Azure Automation connections.</span></span>
<span data-ttu-id="7434a-110">По умолчанию этот командлет извлекает все подключения.</span><span class="sxs-lookup"><span data-stu-id="7434a-110">By default, this cmdlet retrieves all connections.</span></span>
<span data-ttu-id="7434a-111">Укажите имя подключения для получения определенного подключения.</span><span class="sxs-lookup"><span data-stu-id="7434a-111">Specify the name of a connection to get a specific connection.</span></span>
<span data-ttu-id="7434a-112">Укажите имя типа подключения, чтобы получить все соединения определенного типа.</span><span class="sxs-lookup"><span data-stu-id="7434a-112">Specify the connection type name to get all connections of a specific type.</span></span>

## <span data-ttu-id="7434a-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7434a-113">EXAMPLES</span></span>

### <span data-ttu-id="7434a-114">Пример 1: получение всех подключений</span><span class="sxs-lookup"><span data-stu-id="7434a-114">Example 1: Get all connections</span></span>
```
PS C:\>Get-AzureRmAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="7434a-115">Эта команда получает метаданные для всех подключений в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7434a-115">This command gets metadata for all connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="7434a-116">Пример 2: получение всех подключений к типу</span><span class="sxs-lookup"><span data-stu-id="7434a-116">Example 2: Get all connections of a type</span></span>
```
PS C:\>Get-AzureRmAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -ConnectionTypeName "SqlServer"
```

<span data-ttu-id="7434a-117">Эта команда получает метаданные для подключений в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7434a-117">This command gets metadata for connections in the Automation account named Contoso17.</span></span>
<span data-ttu-id="7434a-118">Эта команда получает соединения типа SqlServer.</span><span class="sxs-lookup"><span data-stu-id="7434a-118">This command gets connections of the type SqlServer.</span></span>

### <span data-ttu-id="7434a-119">Пример 3: получение подключения</span><span class="sxs-lookup"><span data-stu-id="7434a-119">Example 3: Get a connection</span></span>
```
PS C:\>Get-AzureRmAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoConnection"
```

<span data-ttu-id="7434a-120">Эта команда получает метаданные для подключения с именем ContosoConnection.</span><span class="sxs-lookup"><span data-stu-id="7434a-120">This command gets metadata for the connection named ContosoConnection.</span></span>

## <span data-ttu-id="7434a-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7434a-121">PARAMETERS</span></span>

### <span data-ttu-id="7434a-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7434a-122">-AutomationAccountName</span></span>
<span data-ttu-id="7434a-123">Указывает имя учетной записи автоматизации, для которой этот командлет получает подключения.</span><span class="sxs-lookup"><span data-stu-id="7434a-123">Specifies the name of the Automation account for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="7434a-124">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="7434a-124">-ConnectionTypeName</span></span>
<span data-ttu-id="7434a-125">Указывает имя типа подключения, для которого этот командлет извлекает подключения.</span><span class="sxs-lookup"><span data-stu-id="7434a-125">Specifies the name of a connection type for which this cmdlet retrieves connections.</span></span>

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

### <span data-ttu-id="7434a-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7434a-126">-Name</span></span>
<span data-ttu-id="7434a-127">Указывает имя подключения, которое этот командлет извлекает.</span><span class="sxs-lookup"><span data-stu-id="7434a-127">Specifies the name of a connection that this cmdlet retrieves.</span></span>

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

### <span data-ttu-id="7434a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7434a-128">-ResourceGroupName</span></span>
<span data-ttu-id="7434a-129">Указывает имя группы ресурсов, для которой этот командлет получает подключения.</span><span class="sxs-lookup"><span data-stu-id="7434a-129">Specifies the name of a resource group for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="7434a-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7434a-130">-DefaultProfile</span></span>
<span data-ttu-id="7434a-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7434a-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7434a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7434a-132">CommonParameters</span></span>
<span data-ttu-id="7434a-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7434a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7434a-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7434a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7434a-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7434a-135">INPUTS</span></span>

## <span data-ttu-id="7434a-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7434a-136">OUTPUTS</span></span>

### <span data-ttu-id="7434a-137">Microsoft. Azure. Commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="7434a-137">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="7434a-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="7434a-138">NOTES</span></span>

## <span data-ttu-id="7434a-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7434a-139">RELATED LINKS</span></span>

[<span data-ttu-id="7434a-140">New-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="7434a-140">New-AzureRmAutomationConnection</span></span>](./New-AzureRMAutomationConnection.md)

[<span data-ttu-id="7434a-141">Remove-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="7434a-141">Remove-AzureRmAutomationConnection</span></span>](./Remove-AzureRMAutomationConnection.md)


