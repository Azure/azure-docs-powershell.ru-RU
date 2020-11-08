---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: BCF8DAB4-3E14-463B-A18F-E91C740B0D3A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 08dd82489bf02efa167386300b9b1d565e1a63de
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076493"
---
# <span data-ttu-id="16033-101">Remove-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="16033-101">Remove-AzureAutomationCertificate</span></span>

## <span data-ttu-id="16033-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="16033-102">SYNOPSIS</span></span>

<span data-ttu-id="16033-103">Удаление сертификата автоматизации.</span><span class="sxs-lookup"><span data-stu-id="16033-103">Removes an Automation certificate.</span></span>

## <span data-ttu-id="16033-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="16033-104">SYNTAX</span></span>

```
Remove-AzureAutomationCertificate -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="16033-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="16033-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="16033-106">Командлет **Remove-AzureAutomationAccount** Удаляет сертификат из службы автоматизации Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="16033-106">The **Remove-AzureAutomationAccount** cmdlet removes a certificate from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="16033-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="16033-107">EXAMPLES</span></span>

### <span data-ttu-id="16033-108">Пример 1: Удаление сертификата</span><span class="sxs-lookup"><span data-stu-id="16033-108">Example 1: Remove a certificate</span></span>
```
PS C:\> Remove-AzureAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01"
```

<span data-ttu-id="16033-109">Эта команда удаляет сертификат с именем Cert01 в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="16033-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="16033-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="16033-110">PARAMETERS</span></span>

### <span data-ttu-id="16033-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="16033-111">-AutomationAccountName</span></span>
<span data-ttu-id="16033-112">Указывает имя учетной записи автоматизации с помощью сертификата.</span><span class="sxs-lookup"><span data-stu-id="16033-112">Specifies the name of the Automation account with the certificate.</span></span>

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

### <span data-ttu-id="16033-113">-Force</span><span class="sxs-lookup"><span data-stu-id="16033-113">-Force</span></span>
<span data-ttu-id="16033-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="16033-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="16033-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="16033-115">-Name</span></span>
<span data-ttu-id="16033-116">Указывает имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="16033-116">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="16033-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="16033-117">-Profile</span></span>
<span data-ttu-id="16033-118">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="16033-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="16033-119">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="16033-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="16033-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16033-120">CommonParameters</span></span>
<span data-ttu-id="16033-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="16033-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16033-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16033-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16033-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="16033-123">INPUTS</span></span>

## <span data-ttu-id="16033-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="16033-124">OUTPUTS</span></span>

## <span data-ttu-id="16033-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="16033-125">NOTES</span></span>

## <span data-ttu-id="16033-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="16033-126">RELATED LINKS</span></span>

[<span data-ttu-id="16033-127">Get-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="16033-127">Get-AzureAutomationCertificate</span></span>](./Get-AzureAutomationCertificate.md)

[<span data-ttu-id="16033-128">New-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="16033-128">New-AzureAutomationCertificate</span></span>](./New-AzureAutomationCertificate.md)

[<span data-ttu-id="16033-129">Set-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="16033-129">Set-AzureAutomationCertificate</span></span>](./Set-AzureAutomationCertificate.md)


