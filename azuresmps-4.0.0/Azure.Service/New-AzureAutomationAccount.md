---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 59CDE74B-EFB3-4904-A482-466B0EA17F4B
online version: ''
schema: 2.0.0
ms.openlocfilehash: a787193669cab32a43b7c9b9eb2010a6e545539b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076224"
---
# <span data-ttu-id="1ecef-101">New-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="1ecef-101">New-AzureAutomationAccount</span></span>

## <span data-ttu-id="1ecef-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1ecef-102">SYNOPSIS</span></span>

<span data-ttu-id="1ecef-103">Создание учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="1ecef-103">Creates an Automation account.</span></span>

## <span data-ttu-id="1ecef-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1ecef-104">SYNTAX</span></span>

```
New-AzureAutomationAccount -Name <String> -Location <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1ecef-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ecef-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="1ecef-106">Командлет **New-AzureAutomationAccount** создает новую учетную запись в службе автоматизации Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1ecef-106">The **New-AzureAutomationAccount** cmdlet creates a new account in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="1ecef-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1ecef-107">EXAMPLES</span></span>

### <span data-ttu-id="1ecef-108">Пример 1: создание учетной записи автоматизации</span><span class="sxs-lookup"><span data-stu-id="1ecef-108">Example 1: Create an Automation account</span></span>
```
PS C:\> New-AzureAutomationAccount -Name "MyAutomationAccount" -Location "East US"
```

<span data-ttu-id="1ecef-109">Эта команда создает учетную запись автоматизации с именем MyAutomationAccount в регионе "Восток США".</span><span class="sxs-lookup"><span data-stu-id="1ecef-109">This command creates an Automation account named MyAutomationAccount in the East US region.</span></span>

## <span data-ttu-id="1ecef-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1ecef-110">PARAMETERS</span></span>

### <span data-ttu-id="1ecef-111">-Location</span><span class="sxs-lookup"><span data-stu-id="1ecef-111">-Location</span></span>
<span data-ttu-id="1ecef-112">Указывает расположение учетной записи.</span><span class="sxs-lookup"><span data-stu-id="1ecef-112">Specifies the location of the account.</span></span>

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

### <span data-ttu-id="1ecef-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1ecef-113">-Name</span></span>
<span data-ttu-id="1ecef-114">Указывает имя учетной записи.</span><span class="sxs-lookup"><span data-stu-id="1ecef-114">Specifies the name of the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ecef-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="1ecef-115">-Profile</span></span>
<span data-ttu-id="1ecef-116">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="1ecef-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1ecef-117">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1ecef-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1ecef-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ecef-118">CommonParameters</span></span>
<span data-ttu-id="1ecef-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1ecef-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ecef-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ecef-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ecef-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1ecef-121">INPUTS</span></span>

## <span data-ttu-id="1ecef-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ecef-122">OUTPUTS</span></span>

### <span data-ttu-id="1ecef-123">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="1ecef-123">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="1ecef-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="1ecef-124">NOTES</span></span>

## <span data-ttu-id="1ecef-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1ecef-125">RELATED LINKS</span></span>

[<span data-ttu-id="1ecef-126">Get-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="1ecef-126">Get-AzureAutomationAccount</span></span>](./Get-AzureAutomationAccount.md)

[<span data-ttu-id="1ecef-127">Remove-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="1ecef-127">Remove-AzureAutomationAccount</span></span>](./Remove-AzureAutomationAccount.md)


