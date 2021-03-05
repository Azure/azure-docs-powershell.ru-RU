---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B32A8423-A7AA-418E-A95D-6C18566741AB
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
ms.openlocfilehash: f88ff018f38040573783aff58287b4788017566a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996999"
---
# <span data-ttu-id="c7b4c-101">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="c7b4c-101">Get-AzAutomationAccount</span></span>

## <span data-ttu-id="c7b4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7b4c-102">SYNOPSIS</span></span>
<span data-ttu-id="c7b4c-103">Получает учетные записи автоматизации в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c7b4c-103">Gets Automation accounts in a resource group.</span></span>

## <span data-ttu-id="c7b4c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c7b4c-104">SYNTAX</span></span>

### <span data-ttu-id="c7b4c-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c7b4c-105">ByAll (Default)</span></span>
```
Get-AzAutomationAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c7b4c-106">ByAutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c7b4c-106">ByAutomationAccountName</span></span>
```
Get-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7b4c-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7b4c-107">DESCRIPTION</span></span>
<span data-ttu-id="c7b4c-108">Для получения учетных записей автоматизации Azure в группе ресурсов возвращается **cmdlet Get-AzAutomationAccount.**</span><span class="sxs-lookup"><span data-stu-id="c7b4c-108">The **Get-AzAutomationAccount** cmdlet gets Azure Automation accounts in a resource group.</span></span>
<span data-ttu-id="c7b4c-109">Дополнительные сведения об учетных записях автоматизации см. в New-AzAutomationAccount>.</span><span class="sxs-lookup"><span data-stu-id="c7b4c-109">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="c7b4c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c7b4c-110">EXAMPLES</span></span>

### <span data-ttu-id="c7b4c-111">Пример 1. Получить все учетные записи</span><span class="sxs-lookup"><span data-stu-id="c7b4c-111">Example 1: Get all accounts</span></span>
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="c7b4c-112">Эта команда получает все учетные записи автоматизации в группе ресурсов ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="c7b4c-112">This command gets all Automation accounts in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="c7b4c-113">Пример 2. Получить учетную запись</span><span class="sxs-lookup"><span data-stu-id="c7b4c-113">Example 2: Get an account</span></span>
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03" -Name "ContosoAutomationAccount"
```

<span data-ttu-id="c7b4c-114">Эта команда получает учетную запись автоматизации ContosoAutomationAccount в группе ресурсов ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c7b4c-114">This command gets the Automation account named ContosoAutomationAccount in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="c7b4c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7b4c-115">PARAMETERS</span></span>

### <span data-ttu-id="c7b4c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7b4c-116">-DefaultProfile</span></span>
<span data-ttu-id="c7b4c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c7b4c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c7b4c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="c7b4c-118">-Name</span></span>
<span data-ttu-id="c7b4c-119">Указывает имя учетной записи автоматизации, которую получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7b4c-119">Specifies the name of the Automation account that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAutomationAccountName
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7b4c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7b4c-120">-ResourceGroupName</span></span>
<span data-ttu-id="c7b4c-121">Указывает имя группы ресурсов, в которой этот cmdlet получает учетные записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="c7b4c-121">Specifies the name of a resource group in which this cmdlet gets Automation accounts.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByAutomationAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7b4c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7b4c-122">CommonParameters</span></span>
<span data-ttu-id="c7b4c-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7b4c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7b4c-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7b4c-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7b4c-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c7b4c-125">INPUTS</span></span>

### <span data-ttu-id="c7b4c-126">System.String</span><span class="sxs-lookup"><span data-stu-id="c7b4c-126">System.String</span></span>

## <span data-ttu-id="c7b4c-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c7b4c-127">OUTPUTS</span></span>

### <span data-ttu-id="c7b4c-128">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="c7b4c-128">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="c7b4c-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c7b4c-129">NOTES</span></span>

## <span data-ttu-id="c7b4c-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c7b4c-130">RELATED LINKS</span></span>

[<span data-ttu-id="c7b4c-131">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="c7b4c-131">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="c7b4c-132">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="c7b4c-132">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)

[<span data-ttu-id="c7b4c-133">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="c7b4c-133">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)


