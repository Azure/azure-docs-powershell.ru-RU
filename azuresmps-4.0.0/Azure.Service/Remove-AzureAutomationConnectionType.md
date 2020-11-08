---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 4370FF88-E34F-499D-AF57-53C15B4EB6E9
online version: ''
schema: 2.0.0
ms.openlocfilehash: e55d9e54dcaa0f547d64ec58b2772a581a8ec30a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076484"
---
# <span data-ttu-id="64e01-101">Remove-AzureAutomationConnectionType</span><span class="sxs-lookup"><span data-stu-id="64e01-101">Remove-AzureAutomationConnectionType</span></span>

## <span data-ttu-id="64e01-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="64e01-102">SYNOPSIS</span></span>

<span data-ttu-id="64e01-103">Удаляет тип подключения.</span><span class="sxs-lookup"><span data-stu-id="64e01-103">Removes a connection type.</span></span>

## <span data-ttu-id="64e01-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="64e01-104">SYNTAX</span></span>

```
Remove-AzureAutomationConnectionType -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="64e01-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="64e01-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="64e01-106">Командлет **Remove-AzureAutomationConnectionType** удаляет тип подключения Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="64e01-106">The **Remove-AzureAutomationConnectionType** cmdlet removes an Azure Automation connection type.</span></span>

## <span data-ttu-id="64e01-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="64e01-107">EXAMPLES</span></span>

## <span data-ttu-id="64e01-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="64e01-108">PARAMETERS</span></span>

### <span data-ttu-id="64e01-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="64e01-109">-AutomationAccountName</span></span>
<span data-ttu-id="64e01-110">Указывает имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="64e01-110">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="64e01-111">-Force</span><span class="sxs-lookup"><span data-stu-id="64e01-111">-Force</span></span>
<span data-ttu-id="64e01-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="64e01-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="64e01-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="64e01-113">-Name</span></span>
<span data-ttu-id="64e01-114">Указывает имя типа подключения, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="64e01-114">Specifies the name of the connection type to remove.</span></span>

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

### <span data-ttu-id="64e01-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="64e01-115">-Profile</span></span>
<span data-ttu-id="64e01-116">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="64e01-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="64e01-117">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="64e01-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="64e01-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64e01-118">CommonParameters</span></span>
<span data-ttu-id="64e01-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="64e01-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64e01-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64e01-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64e01-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="64e01-121">INPUTS</span></span>

## <span data-ttu-id="64e01-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="64e01-122">OUTPUTS</span></span>

## <span data-ttu-id="64e01-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="64e01-123">NOTES</span></span>

## <span data-ttu-id="64e01-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="64e01-124">RELATED LINKS</span></span>

