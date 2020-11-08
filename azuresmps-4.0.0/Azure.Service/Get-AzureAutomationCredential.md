---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C69558DB-78C3-4162-99C3-1300C3FE5287
online version: ''
schema: 2.0.0
ms.openlocfilehash: aa73cf467ffc3675b17b6c59ef5bd07483803267
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075659"
---
# <span data-ttu-id="707b4-101">Get-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="707b4-101">Get-AzureAutomationCredential</span></span>

## <span data-ttu-id="707b4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="707b4-102">SYNOPSIS</span></span>

<span data-ttu-id="707b4-103">Получает учетные данные службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="707b4-103">Gets an Azure Automation credential.</span></span>

## <span data-ttu-id="707b4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="707b4-104">SYNTAX</span></span>

### <span data-ttu-id="707b4-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="707b4-105">ByAll (Default)</span></span>
```
Get-AzureAutomationCredential -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="707b4-106">ByName</span><span class="sxs-lookup"><span data-stu-id="707b4-106">ByName</span></span>
```
Get-AzureAutomationCredential -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="707b4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="707b4-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="707b4-108">Командлет **Get-AzureAutomationCredential** получает одну или несколько учетных данных службы автоматизации Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="707b4-108">The **Get-AzureAutomationCredential** cmdlet gets one or more Microsoft Azure Automation credentials.</span></span>
<span data-ttu-id="707b4-109">По умолчанию возвращаются все учетные данные.</span><span class="sxs-lookup"><span data-stu-id="707b4-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="707b4-110">Чтобы получить определенные учетные данные, укажите его имя.</span><span class="sxs-lookup"><span data-stu-id="707b4-110">To get a specific credential, specify its name.</span></span>

## <span data-ttu-id="707b4-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="707b4-111">EXAMPLES</span></span>

### <span data-ttu-id="707b4-112">Пример 1: получение всех учетных данных</span><span class="sxs-lookup"><span data-stu-id="707b4-112">Example 1: Get all credentials</span></span>
```
PS C:\> Get-AzureAutomationCredential -AutomationAccountName "Contoso17"
```

<span data-ttu-id="707b4-113">Эта команда получает все учетные данные в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="707b4-113">This command gets all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="707b4-114">Пример 2: получение учетных данных</span><span class="sxs-lookup"><span data-stu-id="707b4-114">Example 2: Get a credential</span></span>
```
PS C:\> Get-AzureAutomationCredential -AutomationAccountName "Contoso17" -Name "MyCredential"
```

<span data-ttu-id="707b4-115">Эта команда возвращает учетные данные с именем MyCredential.</span><span class="sxs-lookup"><span data-stu-id="707b4-115">This command gets the credential named MyCredential.</span></span>

## <span data-ttu-id="707b4-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="707b4-116">PARAMETERS</span></span>

### <span data-ttu-id="707b4-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="707b4-117">-AutomationAccountName</span></span>
<span data-ttu-id="707b4-118">Указывает имя учетной записи автоматизации с учетными данными, которые нужно извлечь.</span><span class="sxs-lookup"><span data-stu-id="707b4-118">Specifies the name of the automation account with the credential to retrieve.</span></span>

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

### <span data-ttu-id="707b4-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="707b4-119">-Name</span></span>
<span data-ttu-id="707b4-120">Указывает имя извлекаемых учетных данных.</span><span class="sxs-lookup"><span data-stu-id="707b4-120">Specifies the name of a credential to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="707b4-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="707b4-121">-Profile</span></span>
<span data-ttu-id="707b4-122">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="707b4-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="707b4-123">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="707b4-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="707b4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="707b4-124">CommonParameters</span></span>
<span data-ttu-id="707b4-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="707b4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="707b4-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="707b4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="707b4-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="707b4-127">INPUTS</span></span>

## <span data-ttu-id="707b4-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="707b4-128">OUTPUTS</span></span>

### <span data-ttu-id="707b4-129">Microsoft. Azure. Commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="707b4-129">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="707b4-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="707b4-130">NOTES</span></span>

## <span data-ttu-id="707b4-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="707b4-131">RELATED LINKS</span></span>

[<span data-ttu-id="707b4-132">New-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="707b4-132">New-AzureAutomationCredential</span></span>](./New-AzureAutomationCredential.md)

[<span data-ttu-id="707b4-133">Remove-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="707b4-133">Remove-AzureAutomationCredential</span></span>](./Remove-AzureAutomationCredential.md)

[<span data-ttu-id="707b4-134">Set-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="707b4-134">Set-AzureAutomationCredential</span></span>](./Set-AzureAutomationCredential.md)


