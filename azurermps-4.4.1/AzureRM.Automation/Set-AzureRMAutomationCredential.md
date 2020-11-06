---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D6325A22-2D1B-4228-A5BC-3F1071E26FB2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCredential.md
ms.openlocfilehash: e2a461666edf4f06e78f2bc97f47fcb63ab1c19a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560564"
---
# <span data-ttu-id="5a70e-101">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="5a70e-101">Set-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="5a70e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5a70e-102">SYNOPSIS</span></span>
<span data-ttu-id="5a70e-103">Изменяет учетные данные автоматизации.</span><span class="sxs-lookup"><span data-stu-id="5a70e-103">Modifies an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a70e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5a70e-104">SYNTAX</span></span>

```
Set-AzureRmAutomationCredential [-Name] <String> [-Description <String>] [-Value <PSCredential>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5a70e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a70e-105">DESCRIPTION</span></span>
<span data-ttu-id="5a70e-106">Командлет **Set-AzureRmAutomationCredential** изменяет учетные данные как объект **PSCredential** в службе автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="5a70e-106">The **Set-AzureRmAutomationCredential** cmdlet modifies a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="5a70e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5a70e-107">EXAMPLES</span></span>

### <span data-ttu-id="5a70e-108">Пример 1: обновление учетных данных</span><span class="sxs-lookup"><span data-stu-id="5a70e-108">Example 1: Update a credential</span></span>
```
PS C:\>$User = "Contoso\DChew"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> Set-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01" -Value $Credential
```

<span data-ttu-id="5a70e-109">Первая команда назначает имя пользователя переменной $User.</span><span class="sxs-lookup"><span data-stu-id="5a70e-109">The first command assigns a user name to the $User variable.</span></span>

<span data-ttu-id="5a70e-110">Вторая команда преобразует пароль обычного текста в безопасную строку с помощью командлета ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="5a70e-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="5a70e-111">Команда сохраняет этот объект в переменной $Password.</span><span class="sxs-lookup"><span data-stu-id="5a70e-111">The command stores that object in the $Password variable.</span></span>

<span data-ttu-id="5a70e-112">Третья команда создает учетные данные на основе $User и $Password, а затем сохраняет их в переменной $Credential.</span><span class="sxs-lookup"><span data-stu-id="5a70e-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>

<span data-ttu-id="5a70e-113">Последняя команда изменяет учетные данные автоматизации с именем ContosoCredential, чтобы использовать учетные данные в $Credential.</span><span class="sxs-lookup"><span data-stu-id="5a70e-113">The final command modifies the Automation credential named ContosoCredential to use the credential in $Credential.</span></span>

## <span data-ttu-id="5a70e-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5a70e-114">PARAMETERS</span></span>

### <span data-ttu-id="5a70e-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5a70e-115">-AutomationAccountName</span></span>
<span data-ttu-id="5a70e-116">Указывает имя учетной записи автоматизации, для которой этот командлет изменяет учетные данные.</span><span class="sxs-lookup"><span data-stu-id="5a70e-116">Specifies the name of the Automation account for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="5a70e-117">-Описание</span><span class="sxs-lookup"><span data-stu-id="5a70e-117">-Description</span></span>
<span data-ttu-id="5a70e-118">Задает описание учетных данных, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5a70e-118">Specifies a description for the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="5a70e-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5a70e-119">-Name</span></span>
<span data-ttu-id="5a70e-120">Указывает имя учетных данных, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5a70e-120">Specifies the name of the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="5a70e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a70e-121">-ResourceGroupName</span></span>
<span data-ttu-id="5a70e-122">Указывает имя группы ресурсов, для которой этот командлет изменяет учетные данные.</span><span class="sxs-lookup"><span data-stu-id="5a70e-122">Specifies the name of the resource group for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="5a70e-123">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="5a70e-123">-Value</span></span>
<span data-ttu-id="5a70e-124">Указывает учетные данные как объект **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="5a70e-124">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a70e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a70e-125">-DefaultProfile</span></span>
<span data-ttu-id="5a70e-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5a70e-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a70e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a70e-127">CommonParameters</span></span>
<span data-ttu-id="5a70e-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5a70e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a70e-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a70e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a70e-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5a70e-130">INPUTS</span></span>

## <span data-ttu-id="5a70e-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a70e-131">OUTPUTS</span></span>

### <span data-ttu-id="5a70e-132">Microsoft. Azure. Commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="5a70e-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="5a70e-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="5a70e-133">NOTES</span></span>

## <span data-ttu-id="5a70e-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5a70e-134">RELATED LINKS</span></span>

[<span data-ttu-id="5a70e-135">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="5a70e-135">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="5a70e-136">New-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="5a70e-136">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="5a70e-137">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="5a70e-137">Remove-AzureRmAutomationCredential</span></span>](./Remove-AzureRMAutomationCredential.md)


