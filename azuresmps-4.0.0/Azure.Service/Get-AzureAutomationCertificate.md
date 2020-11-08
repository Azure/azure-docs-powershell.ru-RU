---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: FED10AA9-DD3A-4034-B78E-F9E55290B353
online version: ''
schema: 2.0.0
ms.openlocfilehash: 272969751988d3747788c2a214e8eb7ed509f232
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075663"
---
# <span data-ttu-id="86745-101">Get-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="86745-101">Get-AzureAutomationCertificate</span></span>

## <span data-ttu-id="86745-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="86745-102">SYNOPSIS</span></span>

<span data-ttu-id="86745-103">Получает сертификат службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="86745-103">Gets an Azure Automation certificate.</span></span>

## <span data-ttu-id="86745-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="86745-104">SYNTAX</span></span>

### <span data-ttu-id="86745-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="86745-105">ByAll (Default)</span></span>
```
Get-AzureAutomationCertificate -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="86745-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="86745-106">ByCertificateName</span></span>
```
Get-AzureAutomationCertificate -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="86745-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="86745-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="86745-108">Командлет **Get-AzureAutomationCertificate** получает один или несколько сертификатов службы автоматизации Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="86745-108">The **Get-AzureAutomationCertificate** cmdlet gets one or more Microsoft Azure Automation certificates.</span></span>
<span data-ttu-id="86745-109">По умолчанию возвращаются все сертификаты.</span><span class="sxs-lookup"><span data-stu-id="86745-109">By default, all certificates are returned.</span></span>
<span data-ttu-id="86745-110">Чтобы получить определенный сертификат, укажите его имя.</span><span class="sxs-lookup"><span data-stu-id="86745-110">To get a specific certificate, specify its name.</span></span>

## <span data-ttu-id="86745-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="86745-111">EXAMPLES</span></span>

### <span data-ttu-id="86745-112">Пример 1: получение всех сертификатов</span><span class="sxs-lookup"><span data-stu-id="86745-112">Example 1: Get all certificates</span></span>
```
PS C:\> Get-AzureAutomationCertificate -AutomationAccountName "Contoso17"
```

<span data-ttu-id="86745-113">Эта команда получает все сертификаты в учетной записи службы автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="86745-113">This command gets all certificates in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="86745-114">Пример 2: получение сертификата</span><span class="sxs-lookup"><span data-stu-id="86745-114">Example 2: Get a certificate</span></span>
```
PS C:\> Get-AzureAutomationCertificate -AutomationAccountName "Contoso17" -Name "MyUserCertificate"
```

<span data-ttu-id="86745-115">Эта команда возвращает сертификат с именем MyUserCertificate.</span><span class="sxs-lookup"><span data-stu-id="86745-115">This command gets the certificate named MyUserCertificate.</span></span>

## <span data-ttu-id="86745-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="86745-116">PARAMETERS</span></span>

### <span data-ttu-id="86745-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="86745-117">-AutomationAccountName</span></span>
<span data-ttu-id="86745-118">Указывает имя учетной записи автоматизации с помощью сертификата.</span><span class="sxs-lookup"><span data-stu-id="86745-118">Specifies the name of the automation account with the certificate.</span></span>

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

### <span data-ttu-id="86745-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="86745-119">-Name</span></span>
<span data-ttu-id="86745-120">Указывает имя извлекаемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="86745-120">Specifies the name of a certificate to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86745-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="86745-121">-Profile</span></span>
<span data-ttu-id="86745-122">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="86745-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="86745-123">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="86745-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="86745-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86745-124">CommonParameters</span></span>
<span data-ttu-id="86745-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="86745-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86745-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86745-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86745-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="86745-127">INPUTS</span></span>

## <span data-ttu-id="86745-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="86745-128">OUTPUTS</span></span>

### <span data-ttu-id="86745-129">Microsoft. Azure. Commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="86745-129">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="86745-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="86745-130">NOTES</span></span>

## <span data-ttu-id="86745-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="86745-131">RELATED LINKS</span></span>

[<span data-ttu-id="86745-132">New-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="86745-132">New-AzureAutomationCertificate</span></span>](./New-AzureAutomationCertificate.md)

[<span data-ttu-id="86745-133">Remove-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="86745-133">Remove-AzureAutomationCertificate</span></span>](./Remove-AzureAutomationCertificate.md)

[<span data-ttu-id="86745-134">Set-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="86745-134">Set-AzureAutomationCertificate</span></span>](./Set-AzureAutomationCertificate.md)


