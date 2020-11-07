---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D6325A22-2D1B-4228-A5BC-3F1071E26FB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCredential.md
ms.openlocfilehash: e44b9a5c497aba5533d53acdc9aab31cb5ece703
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93911904"
---
# <span data-ttu-id="3d56f-101">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="3d56f-101">Set-AzAutomationCredential</span></span>

## <span data-ttu-id="3d56f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3d56f-102">SYNOPSIS</span></span>
<span data-ttu-id="3d56f-103">Изменяет учетные данные автоматизации.</span><span class="sxs-lookup"><span data-stu-id="3d56f-103">Modifies an Automation credential.</span></span>

## <span data-ttu-id="3d56f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3d56f-104">SYNTAX</span></span>

```
Set-AzAutomationCredential [-Name] <String> [-Description <String>] [-Value <PSCredential>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3d56f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d56f-105">DESCRIPTION</span></span>
<span data-ttu-id="3d56f-106">Командлет **Set-AzAutomationCredential** изменяет учетные данные как объект **PSCredential** в службе автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="3d56f-106">The **Set-AzAutomationCredential** cmdlet modifies a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="3d56f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3d56f-107">EXAMPLES</span></span>

### <span data-ttu-id="3d56f-108">Пример 1: обновление учетных данных</span><span class="sxs-lookup"><span data-stu-id="3d56f-108">Example 1: Update a credential</span></span>
```
PS C:\>$User = "Contoso\DChew"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> Set-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01" -Value $Credential
```

<span data-ttu-id="3d56f-109">Первая команда назначает имя пользователя переменной $User.</span><span class="sxs-lookup"><span data-stu-id="3d56f-109">The first command assigns a user name to the $User variable.</span></span>
<span data-ttu-id="3d56f-110">Вторая команда преобразует пароль обычного текста в безопасную строку с помощью командлета ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="3d56f-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="3d56f-111">Команда сохраняет этот объект в переменной $Password.</span><span class="sxs-lookup"><span data-stu-id="3d56f-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="3d56f-112">Третья команда создает учетные данные на основе $User и $Password, а затем сохраняет их в переменной $Credential.</span><span class="sxs-lookup"><span data-stu-id="3d56f-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>
<span data-ttu-id="3d56f-113">Последняя команда изменяет учетные данные автоматизации с именем ContosoCredential, чтобы использовать учетные данные в $Credential.</span><span class="sxs-lookup"><span data-stu-id="3d56f-113">The final command modifies the Automation credential named ContosoCredential to use the credential in $Credential.</span></span>

## <span data-ttu-id="3d56f-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3d56f-114">PARAMETERS</span></span>

### <span data-ttu-id="3d56f-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3d56f-115">-AutomationAccountName</span></span>
<span data-ttu-id="3d56f-116">Указывает имя учетной записи автоматизации, для которой этот командлет изменяет учетные данные.</span><span class="sxs-lookup"><span data-stu-id="3d56f-116">Specifies the name of the Automation account for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="3d56f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d56f-117">-DefaultProfile</span></span>
<span data-ttu-id="3d56f-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3d56f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d56f-119">-Описание</span><span class="sxs-lookup"><span data-stu-id="3d56f-119">-Description</span></span>
<span data-ttu-id="3d56f-120">Задает описание учетных данных, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3d56f-120">Specifies a description for the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="3d56f-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3d56f-121">-Name</span></span>
<span data-ttu-id="3d56f-122">Указывает имя учетных данных, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3d56f-122">Specifies the name of the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="3d56f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d56f-123">-ResourceGroupName</span></span>
<span data-ttu-id="3d56f-124">Указывает имя группы ресурсов, для которой этот командлет изменяет учетные данные.</span><span class="sxs-lookup"><span data-stu-id="3d56f-124">Specifies the name of the resource group for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="3d56f-125">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="3d56f-125">-Value</span></span>
<span data-ttu-id="3d56f-126">Указывает учетные данные как объект **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="3d56f-126">Specifies the credentials as a **PSCredential** object.</span></span>

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

### <span data-ttu-id="3d56f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d56f-127">CommonParameters</span></span>
<span data-ttu-id="3d56f-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3d56f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d56f-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d56f-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d56f-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3d56f-130">INPUTS</span></span>

### <span data-ttu-id="3d56f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="3d56f-131">System.String</span></span>

### <span data-ttu-id="3d56f-132">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="3d56f-132">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="3d56f-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d56f-133">OUTPUTS</span></span>

### <span data-ttu-id="3d56f-134">Microsoft. Azure. Commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="3d56f-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="3d56f-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="3d56f-135">NOTES</span></span>

## <span data-ttu-id="3d56f-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3d56f-136">RELATED LINKS</span></span>

[<span data-ttu-id="3d56f-137">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="3d56f-137">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="3d56f-138">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="3d56f-138">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="3d56f-139">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="3d56f-139">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)


