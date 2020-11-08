---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: DDEBA3E1-B5A3-4F16-9A67-A95D15851A33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0899349c3dbfa368b3ce0dbb4d4085c3ea527c43
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076492"
---
# <span data-ttu-id="b83e7-101">Remove-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="b83e7-101">Remove-AzureAutomationConnection</span></span>

## <span data-ttu-id="b83e7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b83e7-102">SYNOPSIS</span></span>

<span data-ttu-id="b83e7-103">Удаляет соединение из автоматизации.</span><span class="sxs-lookup"><span data-stu-id="b83e7-103">Removes a connection from Automation.</span></span>

## <span data-ttu-id="b83e7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b83e7-104">SYNTAX</span></span>

```
Remove-AzureAutomationConnection -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b83e7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b83e7-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="b83e7-106">Командлет **Remove-AzureAutomationConnection** удаляет подключение из службы автоматизации Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b83e7-106">The **Remove-AzureAutomationConnection** cmdlet removes a connection from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="b83e7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b83e7-107">EXAMPLES</span></span>

### <span data-ttu-id="b83e7-108">Пример 1: Удаление соединения</span><span class="sxs-lookup"><span data-stu-id="b83e7-108">Example 1: Remove a connection</span></span>
```
PS C:\> Remove-AzureAutomationConnection -AutomationAccountName "Contoso17" -Name "MyConnection"
```

<span data-ttu-id="b83e7-109">Эта команда удаляет сертификат с именем MyConnection в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="b83e7-109">This command removes a certificate named MyConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="b83e7-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b83e7-110">PARAMETERS</span></span>

### <span data-ttu-id="b83e7-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b83e7-111">-AutomationAccountName</span></span>
<span data-ttu-id="b83e7-112">Указывает имя учетной записи автоматизации с учетными данными.</span><span class="sxs-lookup"><span data-stu-id="b83e7-112">Specifies the name of the Automation account with the credential.</span></span>

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

### <span data-ttu-id="b83e7-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b83e7-113">-Force</span></span>
<span data-ttu-id="b83e7-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="b83e7-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b83e7-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b83e7-115">-Name</span></span>
<span data-ttu-id="b83e7-116">Указывает имя подключения.</span><span class="sxs-lookup"><span data-stu-id="b83e7-116">Specifies the name of the connection.</span></span>

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

### <span data-ttu-id="b83e7-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="b83e7-117">-Profile</span></span>
<span data-ttu-id="b83e7-118">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b83e7-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b83e7-119">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b83e7-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b83e7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b83e7-120">CommonParameters</span></span>
<span data-ttu-id="b83e7-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b83e7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b83e7-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b83e7-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b83e7-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b83e7-123">INPUTS</span></span>

## <span data-ttu-id="b83e7-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b83e7-124">OUTPUTS</span></span>

## <span data-ttu-id="b83e7-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="b83e7-125">NOTES</span></span>

## <span data-ttu-id="b83e7-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b83e7-126">RELATED LINKS</span></span>

[<span data-ttu-id="b83e7-127">Get-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="b83e7-127">Get-AzureAutomationConnection</span></span>](./Get-AzureAutomationConnection.md)

[<span data-ttu-id="b83e7-128">New-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="b83e7-128">New-AzureAutomationConnection</span></span>](./New-AzureAutomationConnection.md)

[<span data-ttu-id="b83e7-129">Set-AzureAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="b83e7-129">Set-AzureAutomationConnectionFieldValue</span></span>](./Set-AzureAutomationConnectionFieldValue.md)


