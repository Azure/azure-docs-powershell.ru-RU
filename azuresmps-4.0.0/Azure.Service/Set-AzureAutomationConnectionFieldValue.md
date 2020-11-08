---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: F80F20B6-21CB-4A37-9CBC-277F6EE99D4B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 421e33bbc74cd70ae6959feb93a0f95f6eac1caf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076427"
---
# <span data-ttu-id="80c79-101">Set-AzureAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="80c79-101">Set-AzureAutomationConnectionFieldValue</span></span>

## <span data-ttu-id="80c79-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="80c79-102">SYNOPSIS</span></span>

<span data-ttu-id="80c79-103">Изменяет значение поля для подключения.</span><span class="sxs-lookup"><span data-stu-id="80c79-103">Modifies the value of a field for a connection.</span></span>

## <span data-ttu-id="80c79-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="80c79-104">SYNTAX</span></span>

```
Set-AzureAutomationConnectionFieldValue -Name <String> -ConnectionFieldName <String> -Value <Object>
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="80c79-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="80c79-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="80c79-106">Командлет **Set-AzureAutomationConnectionFieldValue** изменяет значение поля для подключения в службе автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="80c79-106">The **Set-AzureAutomationConnectionFieldValue** cmdlet modifies the value for a field for a connection in Azure Automation.</span></span>

## <span data-ttu-id="80c79-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="80c79-107">EXAMPLES</span></span>

## <span data-ttu-id="80c79-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="80c79-108">PARAMETERS</span></span>

### <span data-ttu-id="80c79-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="80c79-109">-AutomationAccountName</span></span>
<span data-ttu-id="80c79-110">Указывает имя учетной записи автоматизации с подключением.</span><span class="sxs-lookup"><span data-stu-id="80c79-110">Specifies the name of the Automation account with the connection.</span></span>

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

### <span data-ttu-id="80c79-111">-ConnectionFieldName</span><span class="sxs-lookup"><span data-stu-id="80c79-111">-ConnectionFieldName</span></span>
<span data-ttu-id="80c79-112">Задает имя поля.</span><span class="sxs-lookup"><span data-stu-id="80c79-112">Specifies a name for the field.</span></span>

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

### <span data-ttu-id="80c79-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="80c79-113">-Name</span></span>
<span data-ttu-id="80c79-114">Задает имя для подключения.</span><span class="sxs-lookup"><span data-stu-id="80c79-114">Specifies a name for the connection.</span></span>

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

### <span data-ttu-id="80c79-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="80c79-115">-Profile</span></span>
<span data-ttu-id="80c79-116">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="80c79-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="80c79-117">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="80c79-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="80c79-118">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="80c79-118">-Value</span></span>
<span data-ttu-id="80c79-119">Задает значение, которое будет храниться в поле Connection (соединение).</span><span class="sxs-lookup"><span data-stu-id="80c79-119">Specifies a value to store in the connection field.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80c79-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80c79-120">CommonParameters</span></span>
<span data-ttu-id="80c79-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="80c79-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80c79-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80c79-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80c79-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="80c79-123">INPUTS</span></span>

## <span data-ttu-id="80c79-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="80c79-124">OUTPUTS</span></span>

## <span data-ttu-id="80c79-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="80c79-125">NOTES</span></span>

## <span data-ttu-id="80c79-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="80c79-126">RELATED LINKS</span></span>

[<span data-ttu-id="80c79-127">Get-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="80c79-127">Get-AzureAutomationConnection</span></span>](./Get-AzureAutomationConnection.md)

[<span data-ttu-id="80c79-128">New-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="80c79-128">New-AzureAutomationConnection</span></span>](./New-AzureAutomationConnection.md)

[<span data-ttu-id="80c79-129">Remove-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="80c79-129">Remove-AzureAutomationConnection</span></span>](./Remove-AzureAutomationConnection.md)


