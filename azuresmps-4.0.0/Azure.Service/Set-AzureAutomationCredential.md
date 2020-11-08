---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C92B4B70-4342-4219-80D3-FB79BDC171A3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 16fbdf1a0a63fb5a75aa7bc200036a7332ea15f8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075831"
---
# <span data-ttu-id="04d10-101">Set-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="04d10-101">Set-AzureAutomationCredential</span></span>

## <span data-ttu-id="04d10-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="04d10-102">SYNOPSIS</span></span>

<span data-ttu-id="04d10-103">Изменение учетных данных в автоматизации.</span><span class="sxs-lookup"><span data-stu-id="04d10-103">Modifies a credential in Automation.</span></span>

## <span data-ttu-id="04d10-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="04d10-104">SYNTAX</span></span>

```
Set-AzureAutomationCredential -Name <String> [-Description <String>] [-Value <PSCredential>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="04d10-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="04d10-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="04d10-106">Командлет **Set-AzureAutomationCredential** изменяет учетные данные как объект **PSCredential** в Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="04d10-106">The **Set-AzureAutomationCredential** cmdlet modifies a credential as a **PSCredential** object in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="04d10-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="04d10-107">EXAMPLES</span></span>

### <span data-ttu-id="04d10-108">Пример 1: обновление учетных данных</span><span class="sxs-lookup"><span data-stu-id="04d10-108">Example 1: Update a credential</span></span>
```
PS C:\> $user = "MyDomain\MyUser"
PS C:\> $pw = ConvertTo-SecureString "PassWord!" -AsPlainText -Force
PS C:\> $cred = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $user, $pw
PS C:\> New-AzureAutomationCredential -AutomationAccountName "Contos17" -Name "MyCredential" -Value $cred
```

<span data-ttu-id="04d10-109">Эти команды используются для обновления существующих учетных данных с именем MyCredential.</span><span class="sxs-lookup"><span data-stu-id="04d10-109">These commands update an existing credential named MyCredential.</span></span>
<span data-ttu-id="04d10-110">Сначала создается объект учетных данных, включающий имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="04d10-110">A credential object is first created that includes a username and password.</span></span>
<span data-ttu-id="04d10-111">Затем она используется в последней команде для обновления учетных данных автоматизации.</span><span class="sxs-lookup"><span data-stu-id="04d10-111">This is then used in the last command to update the automation credential.</span></span>

## <span data-ttu-id="04d10-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="04d10-112">PARAMETERS</span></span>

### <span data-ttu-id="04d10-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="04d10-113">-AutomationAccountName</span></span>
<span data-ttu-id="04d10-114">Указывает имя учетной записи автоматизации с учетными данными.</span><span class="sxs-lookup"><span data-stu-id="04d10-114">Specifies the name of the Automation account with the credential.</span></span>

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

### <span data-ttu-id="04d10-115">-Описание</span><span class="sxs-lookup"><span data-stu-id="04d10-115">-Description</span></span>
<span data-ttu-id="04d10-116">Задает описание учетных данных.</span><span class="sxs-lookup"><span data-stu-id="04d10-116">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="04d10-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="04d10-117">-Name</span></span>
<span data-ttu-id="04d10-118">Указывает имя учетных данных.</span><span class="sxs-lookup"><span data-stu-id="04d10-118">Specifies the name of the credential.</span></span>

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

### <span data-ttu-id="04d10-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="04d10-119">-Profile</span></span>
<span data-ttu-id="04d10-120">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="04d10-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="04d10-121">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="04d10-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="04d10-122">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="04d10-122">-Value</span></span>
<span data-ttu-id="04d10-123">Указывает учетные данные как объект **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="04d10-123">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04d10-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04d10-124">CommonParameters</span></span>
<span data-ttu-id="04d10-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="04d10-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04d10-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04d10-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04d10-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="04d10-127">INPUTS</span></span>

## <span data-ttu-id="04d10-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="04d10-128">OUTPUTS</span></span>

### <span data-ttu-id="04d10-129">Microsoft. Azure. Commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="04d10-129">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="04d10-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="04d10-130">NOTES</span></span>

## <span data-ttu-id="04d10-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="04d10-131">RELATED LINKS</span></span>

[<span data-ttu-id="04d10-132">Get-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="04d10-132">Get-AzureAutomationCredential</span></span>](./Get-AzureAutomationCredential.md)

[<span data-ttu-id="04d10-133">New-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="04d10-133">New-AzureAutomationCredential</span></span>](./New-AzureAutomationCredential.md)

[<span data-ttu-id="04d10-134">Remove-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="04d10-134">Remove-AzureAutomationCredential</span></span>](./Remove-AzureAutomationCredential.md)


