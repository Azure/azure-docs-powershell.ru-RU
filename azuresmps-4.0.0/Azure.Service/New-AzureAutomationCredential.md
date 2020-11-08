---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: E42F05D0-28AD-4772-9F53-BCE6EFC698AF
online version: ''
schema: 2.0.0
ms.openlocfilehash: bc7d44b87c1e371f0d0c065746dae991cff1cca8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076221"
---
# <span data-ttu-id="6917e-101">New-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="6917e-101">New-AzureAutomationCredential</span></span>

## <span data-ttu-id="6917e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6917e-102">SYNOPSIS</span></span>

<span data-ttu-id="6917e-103">Создает учетные данные в автоматизации.</span><span class="sxs-lookup"><span data-stu-id="6917e-103">Creates a credential in Automation.</span></span>

## <span data-ttu-id="6917e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6917e-104">SYNTAX</span></span>

```
New-AzureAutomationCredential -Name <String> [-Description <String>] -Value <PSCredential>
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6917e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6917e-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="6917e-106">Командлет **New-AzureAutomationCredential** создает учетные данные как объект **PSCredential** в службе автоматизации Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6917e-106">The **New-AzureAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="6917e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6917e-107">EXAMPLES</span></span>

### <span data-ttu-id="6917e-108">Пример 1: создание учетных данных</span><span class="sxs-lookup"><span data-stu-id="6917e-108">Example 1: Create a credential</span></span>
```
PS C:\> $user = "MyDomain\MyUser"
PS C:\> $pw = ConvertTo-SecureString "PassWord!" -AsPlainText -Force
PS C:\> $cred = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $user, $pw
PS C:\> New-AzureAutomationCredential -AutomationAccountName "Contoso17" -Name "MyCredential" -Value $cred
```

<span data-ttu-id="6917e-109">Эти команды создают учетные данные с именем MyCredential.</span><span class="sxs-lookup"><span data-stu-id="6917e-109">These commands create a credential named MyCredential.</span></span>
<span data-ttu-id="6917e-110">Сначала создается объект учетных данных, включающий имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="6917e-110">A credential object is first created that includes a username and password.</span></span>
<span data-ttu-id="6917e-111">Затем она используется в последней команде для создания учетных данных автоматизации.</span><span class="sxs-lookup"><span data-stu-id="6917e-111">This is then used in the last command to create the Automation credential.</span></span>

## <span data-ttu-id="6917e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6917e-112">PARAMETERS</span></span>

### <span data-ttu-id="6917e-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6917e-113">-AutomationAccountName</span></span>
<span data-ttu-id="6917e-114">Указывает имя учетной записи автоматизации, в которой будут храниться учетные данные.</span><span class="sxs-lookup"><span data-stu-id="6917e-114">Specifies the name of the Automation account the credential will be stored in.</span></span>

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

### <span data-ttu-id="6917e-115">-Описание</span><span class="sxs-lookup"><span data-stu-id="6917e-115">-Description</span></span>
<span data-ttu-id="6917e-116">Задает описание учетных данных.</span><span class="sxs-lookup"><span data-stu-id="6917e-116">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="6917e-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6917e-117">-Name</span></span>
<span data-ttu-id="6917e-118">Задает имя для учетных данных.</span><span class="sxs-lookup"><span data-stu-id="6917e-118">Specifies a name for the credential.</span></span>

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

### <span data-ttu-id="6917e-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="6917e-119">-Profile</span></span>
<span data-ttu-id="6917e-120">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6917e-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6917e-121">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6917e-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6917e-122">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="6917e-122">-Value</span></span>
<span data-ttu-id="6917e-123">Указывает учетные данные как объект **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="6917e-123">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6917e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6917e-124">CommonParameters</span></span>
<span data-ttu-id="6917e-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6917e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6917e-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6917e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6917e-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6917e-127">INPUTS</span></span>

## <span data-ttu-id="6917e-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6917e-128">OUTPUTS</span></span>

### <span data-ttu-id="6917e-129">Microsoft. Azure. Commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="6917e-129">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="6917e-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="6917e-130">NOTES</span></span>

## <span data-ttu-id="6917e-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6917e-131">RELATED LINKS</span></span>

[<span data-ttu-id="6917e-132">Get-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="6917e-132">Get-AzureAutomationCredential</span></span>](./Get-AzureAutomationCredential.md)

[<span data-ttu-id="6917e-133">Remove-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="6917e-133">Remove-AzureAutomationCredential</span></span>](./Remove-AzureAutomationCredential.md)

[<span data-ttu-id="6917e-134">Set-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="6917e-134">Set-AzureAutomationCredential</span></span>](./Set-AzureAutomationCredential.md)


