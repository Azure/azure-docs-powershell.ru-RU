---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 4D87DD30-4AEF-4269-93B2-AE5964334AC8
online version: ''
schema: 2.0.0
ms.openlocfilehash: b581712f020b8168c052634e0f20244e16a7d950
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076480"
---
# <span data-ttu-id="bbd36-101">Remove-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="bbd36-101">Remove-AzureAutomationCredential</span></span>

## <span data-ttu-id="bbd36-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bbd36-102">SYNOPSIS</span></span>

<span data-ttu-id="bbd36-103">Удаление учетных данных из автоматизации.</span><span class="sxs-lookup"><span data-stu-id="bbd36-103">Removes a credential from Automation.</span></span>

## <span data-ttu-id="bbd36-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bbd36-104">SYNTAX</span></span>

```
Remove-AzureAutomationCredential -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bbd36-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bbd36-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="bbd36-106">Командлет **Remove-AzureAutomationCredential** удаляет учетные данные из службы автоматизации Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="bbd36-106">The **Remove-AzureAutomationCredential** cmdlet removes a credential from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="bbd36-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bbd36-107">EXAMPLES</span></span>

### <span data-ttu-id="bbd36-108">Пример 1: удаление учетных данных</span><span class="sxs-lookup"><span data-stu-id="bbd36-108">Example 1: Remove a credential</span></span>
```
PS C:\> Remove-AzureAutomationCredential -AutomationAccountName "Contoso17" -Name "MyCredential"
```

<span data-ttu-id="bbd36-109">Эта команда удаляет учетные данные с именем MyCredential в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="bbd36-109">This command removes a credential named MyCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="bbd36-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bbd36-110">PARAMETERS</span></span>

### <span data-ttu-id="bbd36-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bbd36-111">-AutomationAccountName</span></span>
<span data-ttu-id="bbd36-112">Указывает имя учетной записи автоматизации с учетными данными.</span><span class="sxs-lookup"><span data-stu-id="bbd36-112">Specifies the name of the Automation account with the credential.</span></span>

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

### <span data-ttu-id="bbd36-113">-Force</span><span class="sxs-lookup"><span data-stu-id="bbd36-113">-Force</span></span>
<span data-ttu-id="bbd36-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="bbd36-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bbd36-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bbd36-115">-Name</span></span>
<span data-ttu-id="bbd36-116">Указывает имя учетных данных, которые нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="bbd36-116">Specifies the name of the credential to remove.</span></span>

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

### <span data-ttu-id="bbd36-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="bbd36-117">-Profile</span></span>
<span data-ttu-id="bbd36-118">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="bbd36-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bbd36-119">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bbd36-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bbd36-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbd36-120">CommonParameters</span></span>
<span data-ttu-id="bbd36-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bbd36-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbd36-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbd36-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbd36-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bbd36-123">INPUTS</span></span>

## <span data-ttu-id="bbd36-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bbd36-124">OUTPUTS</span></span>

## <span data-ttu-id="bbd36-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="bbd36-125">NOTES</span></span>

## <span data-ttu-id="bbd36-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bbd36-126">RELATED LINKS</span></span>

[<span data-ttu-id="bbd36-127">Get-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="bbd36-127">Get-AzureAutomationCredential</span></span>](./Get-AzureAutomationCredential.md)

[<span data-ttu-id="bbd36-128">New-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="bbd36-128">New-AzureAutomationCredential</span></span>](./New-AzureAutomationCredential.md)

[<span data-ttu-id="bbd36-129">Set-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="bbd36-129">Set-AzureAutomationCredential</span></span>](./Set-AzureAutomationCredential.md)


