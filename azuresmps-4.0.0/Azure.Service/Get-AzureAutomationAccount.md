---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 7B2D9768-919B-4F54-BBC7-8882CC2C973A
online version: ''
schema: 2.0.0
ms.openlocfilehash: a9ce55e573881a29291085e9bf25381170bbf052
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076371"
---
# <span data-ttu-id="71344-101">Get-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="71344-101">Get-AzureAutomationAccount</span></span>

## <span data-ttu-id="71344-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="71344-102">SYNOPSIS</span></span>

<span data-ttu-id="71344-103">Возвращает учетные записи службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="71344-103">Gets Azure Automation accounts.</span></span>

## <span data-ttu-id="71344-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="71344-104">SYNTAX</span></span>

```
Get-AzureAutomationAccount [-Name <String>] [-Location <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="71344-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="71344-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="71344-106">Командлет **Get-AzureAutomationAccount** получает учетные записи службы автоматизации Microsoft Azure для вашей подписки.</span><span class="sxs-lookup"><span data-stu-id="71344-106">The **Get-AzureAutomationAccount** cmdlet gets the Microsoft Azure Automation accounts for your subscription.</span></span>
<span data-ttu-id="71344-107">Учетная запись автоматизации является контейнером для ресурсов автоматизации, которые изолированы от ресурсов других учетных записей автоматизации.</span><span class="sxs-lookup"><span data-stu-id="71344-107">An Automation account is a container for Automation resources that is isolated from the resources of other Automation accounts.</span></span>
<span data-ttu-id="71344-108">Ресурсы автоматизации включают Runbook, задания и ресурсы.</span><span class="sxs-lookup"><span data-stu-id="71344-108">Automation resources include runbooks, jobs, and assets.</span></span>

## <span data-ttu-id="71344-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="71344-109">EXAMPLES</span></span>

### <span data-ttu-id="71344-110">Пример 1: получение учетной записи автоматизации</span><span class="sxs-lookup"><span data-stu-id="71344-110">Example 1: Get an Automation account</span></span>
```
PS C:\> Get-AzureAutomationAccount -Name "Contoso17"
```

<span data-ttu-id="71344-111">Эта команда получает учетную запись автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="71344-111">This command gets the Automation account named Contoso17.</span></span>

## <span data-ttu-id="71344-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="71344-112">PARAMETERS</span></span>

### <span data-ttu-id="71344-113">-Location</span><span class="sxs-lookup"><span data-stu-id="71344-113">-Location</span></span>
<span data-ttu-id="71344-114">Указывает расположение Azure, связанное с учетными записями автоматизации.</span><span class="sxs-lookup"><span data-stu-id="71344-114">Specifies an Azure location associated with Automation accounts.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71344-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="71344-115">-Name</span></span>
<span data-ttu-id="71344-116">Указывает имя учетной записи службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="71344-116">Specifies the name of an Azure Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71344-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="71344-117">-Profile</span></span>
<span data-ttu-id="71344-118">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="71344-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="71344-119">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="71344-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="71344-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71344-120">CommonParameters</span></span>
<span data-ttu-id="71344-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="71344-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71344-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71344-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71344-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="71344-123">INPUTS</span></span>

## <span data-ttu-id="71344-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="71344-124">OUTPUTS</span></span>

### <span data-ttu-id="71344-125">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="71344-125">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="71344-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="71344-126">NOTES</span></span>

## <span data-ttu-id="71344-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="71344-127">RELATED LINKS</span></span>

[<span data-ttu-id="71344-128">New-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="71344-128">New-AzureAutomationAccount</span></span>](./New-AzureAutomationAccount.md)

[<span data-ttu-id="71344-129">Remove-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="71344-129">Remove-AzureAutomationAccount</span></span>](./Remove-AzureAutomationAccount.md)


