---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D6325A22-2D1B-4228-A5BC-3F1071E26FB2
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCredential.md
ms.openlocfilehash: 6fbef2bcedf4de93cd816f6a4702ee01df10d17f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957720"
---
# <span data-ttu-id="35998-101">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="35998-101">Set-AzAutomationCredential</span></span>

## <span data-ttu-id="35998-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35998-102">SYNOPSIS</span></span>
<span data-ttu-id="35998-103">Изменяет учетные данные автоматизации.</span><span class="sxs-lookup"><span data-stu-id="35998-103">Modifies an Automation credential.</span></span>

## <span data-ttu-id="35998-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="35998-104">SYNTAX</span></span>

```
Set-AzAutomationCredential [-Name] <String> [-Description <String>] [-Value <PSCredential>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="35998-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35998-105">DESCRIPTION</span></span>
<span data-ttu-id="35998-106">**Cmdlet Set-AzAutomationCredential** изменяет учетные данные как **объект PSCredential** в автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="35998-106">The **Set-AzAutomationCredential** cmdlet modifies a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="35998-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="35998-107">EXAMPLES</span></span>

### <span data-ttu-id="35998-108">Пример 1. Обновление учетных данных</span><span class="sxs-lookup"><span data-stu-id="35998-108">Example 1: Update a credential</span></span>
```
PS C:\>$User = "Contoso\DChew"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> Set-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01" -Value $Credential
```

<span data-ttu-id="35998-109">Первая команда назначает имя пользователя переменной $User.</span><span class="sxs-lookup"><span data-stu-id="35998-109">The first command assigns a user name to the $User variable.</span></span>
<span data-ttu-id="35998-110">Вторая команда преобразует пароль в виде обычного текста в безопасную строку с помощью ConvertTo-SecureString командлета.</span><span class="sxs-lookup"><span data-stu-id="35998-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="35998-111">Эта команда сохраняет объект в переменной $Password.</span><span class="sxs-lookup"><span data-stu-id="35998-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="35998-112">Третья команда создает учетные данные на основе $User и $Password, а затем сохраняет их в $Credential переменной.</span><span class="sxs-lookup"><span data-stu-id="35998-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>
<span data-ttu-id="35998-113">Конечная команда изменяет учетные данные автоматизации с именем ContosoCredential для использования учетных данных в $Credential.</span><span class="sxs-lookup"><span data-stu-id="35998-113">The final command modifies the Automation credential named ContosoCredential to use the credential in $Credential.</span></span>

## <span data-ttu-id="35998-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35998-114">PARAMETERS</span></span>

### <span data-ttu-id="35998-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="35998-115">-AutomationAccountName</span></span>
<span data-ttu-id="35998-116">Указывает имя учетной записи автоматизации, для которой этот cmdlet изменяет учетные данные.</span><span class="sxs-lookup"><span data-stu-id="35998-116">Specifies the name of the Automation account for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="35998-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35998-117">-DefaultProfile</span></span>
<span data-ttu-id="35998-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="35998-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35998-119">-Description</span><span class="sxs-lookup"><span data-stu-id="35998-119">-Description</span></span>
<span data-ttu-id="35998-120">Описание учетных данных, которые изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35998-120">Specifies a description for the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="35998-121">-Name</span><span class="sxs-lookup"><span data-stu-id="35998-121">-Name</span></span>
<span data-ttu-id="35998-122">Указывает имя учетных данных, которые изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35998-122">Specifies the name of the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="35998-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35998-123">-ResourceGroupName</span></span>
<span data-ttu-id="35998-124">Имя группы ресурсов, для которой этот cmdlet изменяет учетные данные.</span><span class="sxs-lookup"><span data-stu-id="35998-124">Specifies the name of the resource group for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="35998-125">-Значение</span><span class="sxs-lookup"><span data-stu-id="35998-125">-Value</span></span>
<span data-ttu-id="35998-126">Определяет учетные данные как **объект PSCredential.**</span><span class="sxs-lookup"><span data-stu-id="35998-126">Specifies the credentials as a **PSCredential** object.</span></span>

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

### <span data-ttu-id="35998-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35998-127">CommonParameters</span></span>
<span data-ttu-id="35998-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35998-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35998-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35998-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35998-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="35998-130">INPUTS</span></span>

### <span data-ttu-id="35998-131">System.String</span><span class="sxs-lookup"><span data-stu-id="35998-131">System.String</span></span>

### <span data-ttu-id="35998-132">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="35998-132">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="35998-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="35998-133">OUTPUTS</span></span>

### <span data-ttu-id="35998-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="35998-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="35998-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="35998-135">NOTES</span></span>

## <span data-ttu-id="35998-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35998-136">RELATED LINKS</span></span>

[<span data-ttu-id="35998-137">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="35998-137">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="35998-138">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="35998-138">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="35998-139">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="35998-139">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)


