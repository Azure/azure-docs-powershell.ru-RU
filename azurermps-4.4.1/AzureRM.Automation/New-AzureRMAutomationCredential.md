---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 739EB137-E4A8-4E85-96BD-4CF26D2C5763
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCredential.md
ms.openlocfilehash: cb332c1aed8f828f893417561302ddcf36ba0cdb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565685"
---
# <span data-ttu-id="c4cf4-101">New-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="c4cf4-101">New-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="c4cf4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c4cf4-102">SYNOPSIS</span></span>
<span data-ttu-id="c4cf4-103">Создает учетные данные автоматизации.</span><span class="sxs-lookup"><span data-stu-id="c4cf4-103">Creates an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4cf4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c4cf4-104">SYNTAX</span></span>

```
New-AzureRmAutomationCredential [-Name] <String> [-Description <String>] [-Value] <PSCredential>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c4cf4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4cf4-105">DESCRIPTION</span></span>
<span data-ttu-id="c4cf4-106">Командлет **New-AzureRmAutomationCredential** создает учетные данные как объект **PSCredential** в службе автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="c4cf4-106">The **New-AzureRmAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="c4cf4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c4cf4-107">EXAMPLES</span></span>

### <span data-ttu-id="c4cf4-108">Пример 1: создание учетных данных</span><span class="sxs-lookup"><span data-stu-id="c4cf4-108">Example 1: Create a credential</span></span>
```
PS C:\>$User = "Contoso\PFuller"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> New-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -Value $Credential -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="c4cf4-109">Первая команда назначает имя пользователя переменной $User.</span><span class="sxs-lookup"><span data-stu-id="c4cf4-109">The first command assigns a user name to the $User variable.</span></span>

<span data-ttu-id="c4cf4-110">Вторая команда преобразует пароль обычного текста в безопасную строку с помощью командлета ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="c4cf4-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="c4cf4-111">Команда сохраняет этот объект в переменной $Password.</span><span class="sxs-lookup"><span data-stu-id="c4cf4-111">The command stores that object in the $Password variable.</span></span>

<span data-ttu-id="c4cf4-112">Третья команда создает учетные данные на основе $User и $Password, а затем сохраняет их в переменной $Credential.</span><span class="sxs-lookup"><span data-stu-id="c4cf4-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>

<span data-ttu-id="c4cf4-113">Последняя команда создает учетные данные автоматизации с именем ContosoCredential, которая использует $Credential.</span><span class="sxs-lookup"><span data-stu-id="c4cf4-113">The final command creates an Automation credential named ContosoCredential that uses $Credential.</span></span>

## <span data-ttu-id="c4cf4-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c4cf4-114">PARAMETERS</span></span>

### <span data-ttu-id="c4cf4-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c4cf4-115">-AutomationAccountName</span></span>
<span data-ttu-id="c4cf4-116">Указывает имя учетной записи автоматизации, в которой этот командлет хранит учетные данные.</span><span class="sxs-lookup"><span data-stu-id="c4cf4-116">Specifies the name of the Automation account in which this cmdlet stores the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4cf4-117">-Описание</span><span class="sxs-lookup"><span data-stu-id="c4cf4-117">-Description</span></span>
<span data-ttu-id="c4cf4-118">Задает описание учетных данных.</span><span class="sxs-lookup"><span data-stu-id="c4cf4-118">Specifies a description for the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4cf4-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c4cf4-119">-Name</span></span>
<span data-ttu-id="c4cf4-120">Задает имя для учетных данных.</span><span class="sxs-lookup"><span data-stu-id="c4cf4-120">Specifies a name for the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4cf4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4cf4-121">-ResourceGroupName</span></span>
<span data-ttu-id="c4cf4-122">Задает описание группы ресурсов, для которой этот командлет создает учетные данные.</span><span class="sxs-lookup"><span data-stu-id="c4cf4-122">Specifies a description for the resource group for which this cmdlet creates a credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4cf4-123">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="c4cf4-123">-Value</span></span>
<span data-ttu-id="c4cf4-124">Указывает учетные данные как объект **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="c4cf4-124">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4cf4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4cf4-125">-DefaultProfile</span></span>
<span data-ttu-id="c4cf4-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c4cf4-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4cf4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4cf4-127">CommonParameters</span></span>
<span data-ttu-id="c4cf4-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c4cf4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4cf4-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4cf4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4cf4-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c4cf4-130">INPUTS</span></span>

## <span data-ttu-id="c4cf4-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4cf4-131">OUTPUTS</span></span>

### <span data-ttu-id="c4cf4-132">Microsoft. Azure. Commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="c4cf4-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="c4cf4-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="c4cf4-133">NOTES</span></span>

## <span data-ttu-id="c4cf4-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c4cf4-134">RELATED LINKS</span></span>

[<span data-ttu-id="c4cf4-135">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="c4cf4-135">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="c4cf4-136">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="c4cf4-136">Remove-AzureRmAutomationCredential</span></span>](./Remove-AzureRMAutomationCredential.md)

[<span data-ttu-id="c4cf4-137">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="c4cf4-137">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)


