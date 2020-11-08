---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: DD881317-7366-4B55-B1CC-6AF0286F1C5D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 69ef6fc78280180a3722492e5a4b53a52c7bde2a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076370"
---
# <span data-ttu-id="f8227-101">Get-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="f8227-101">Get-AzureAutomationConnection</span></span>

## <span data-ttu-id="f8227-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f8227-102">SYNOPSIS</span></span>

<span data-ttu-id="f8227-103">Получает подключение Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="f8227-103">Gets an Azure Automation connection.</span></span>

## <span data-ttu-id="f8227-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f8227-104">SYNTAX</span></span>

### <span data-ttu-id="f8227-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f8227-105">ByAll (Default)</span></span>
```
Get-AzureAutomationConnection -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f8227-106">ByConnectionName</span><span class="sxs-lookup"><span data-stu-id="f8227-106">ByConnectionName</span></span>
```
Get-AzureAutomationConnection -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="f8227-107">ByConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="f8227-107">ByConnectionTypeName</span></span>
```
Get-AzureAutomationConnection -ConnectionTypeName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f8227-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8227-108">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="f8227-109">Командлет **Get-AzureAutomationConnection** получает одно или несколько подключений службы автоматизации Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f8227-109">The **Get-AzureAutomationConnection** cmdlet gets one or more Microsoft Azure Automation connections.</span></span>
<span data-ttu-id="f8227-110">По умолчанию возвращаются все подключения.</span><span class="sxs-lookup"><span data-stu-id="f8227-110">By default, all connections are returned.</span></span>
<span data-ttu-id="f8227-111">Чтобы получить конкретное подключение, укажите его имя.</span><span class="sxs-lookup"><span data-stu-id="f8227-111">To get a specific connection, specify its name.</span></span>
<span data-ttu-id="f8227-112">Чтобы получить все соединения определенного типа, укажите имя типа подключения.</span><span class="sxs-lookup"><span data-stu-id="f8227-112">To get all connections of a certain type, specify the connection type name.</span></span>

## <span data-ttu-id="f8227-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f8227-113">EXAMPLES</span></span>

### <span data-ttu-id="f8227-114">Пример 1: получение всех подключений</span><span class="sxs-lookup"><span data-stu-id="f8227-114">Example 1: Get all connections</span></span>
```
PS C:\> Get-AzureAutomationConnection -AutomationAccountName "Contoso17"
```

<span data-ttu-id="f8227-115">Эта команда получает все подключения в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f8227-115">This command gets all connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="f8227-116">Пример 2: получение всех подключений к типу</span><span class="sxs-lookup"><span data-stu-id="f8227-116">Example 2: Get all connections of a type</span></span>
```
PS C:\> Get-AzureAutomationConnection -AutomationAccountName "Contoso17" -ConnectionTypeName "Azure"
```

<span data-ttu-id="f8227-117">Эта команда получает все подключения Azure в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f8227-117">This command gets all Azure connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="f8227-118">Пример 3: получение подключения</span><span class="sxs-lookup"><span data-stu-id="f8227-118">Example 3: Get a connection</span></span>
```
PS C:\> Get-AzureAutomationConnection -AutomationAccountName "Contoso17" -Name "Azure"
```

<span data-ttu-id="f8227-119">Эта команда получает подключение с именем MyConnection.</span><span class="sxs-lookup"><span data-stu-id="f8227-119">This command gets the connection named MyConnection.</span></span>

## <span data-ttu-id="f8227-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f8227-120">PARAMETERS</span></span>

### <span data-ttu-id="f8227-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f8227-121">-AutomationAccountName</span></span>
<span data-ttu-id="f8227-122">Указывает имя учетной записи автоматизации с подключением для извлечения.</span><span class="sxs-lookup"><span data-stu-id="f8227-122">Specifies the name of the automation account with the connection to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8227-123">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="f8227-123">-ConnectionTypeName</span></span>
<span data-ttu-id="f8227-124">Указывает имя типа соединения для загружаемых подключений.</span><span class="sxs-lookup"><span data-stu-id="f8227-124">Specifies the name of a connection type for the connections to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionTypeName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8227-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f8227-125">-Name</span></span>
<span data-ttu-id="f8227-126">Указывает имя загружаемого подключения.</span><span class="sxs-lookup"><span data-stu-id="f8227-126">Specifies the name of a connection to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8227-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="f8227-127">-Profile</span></span>
<span data-ttu-id="f8227-128">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f8227-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f8227-129">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f8227-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8227-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8227-130">CommonParameters</span></span>
<span data-ttu-id="f8227-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f8227-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8227-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8227-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8227-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f8227-133">INPUTS</span></span>

## <span data-ttu-id="f8227-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8227-134">OUTPUTS</span></span>

### <span data-ttu-id="f8227-135">Microsoft. Azure. Commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="f8227-135">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="f8227-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="f8227-136">NOTES</span></span>

## <span data-ttu-id="f8227-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f8227-137">RELATED LINKS</span></span>

[<span data-ttu-id="f8227-138">New-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="f8227-138">New-AzureAutomationConnection</span></span>](./New-AzureAutomationConnection.md)

[<span data-ttu-id="f8227-139">Remove-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="f8227-139">Remove-AzureAutomationConnection</span></span>](./Remove-AzureAutomationConnection.md)

[<span data-ttu-id="f8227-140">Set-AzureAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="f8227-140">Set-AzureAutomationConnectionFieldValue</span></span>](./Set-AzureAutomationConnectionFieldValue.md)


