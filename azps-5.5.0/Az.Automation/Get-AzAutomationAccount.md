---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B32A8423-A7AA-418E-A95D-6C18566741AB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
ms.openlocfilehash: 46d6ba805b6995c0d984149d699ce0679f682407
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100235300"
---
# <span data-ttu-id="8985e-101">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8985e-101">Get-AzAutomationAccount</span></span>

## <span data-ttu-id="8985e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8985e-102">SYNOPSIS</span></span>
<span data-ttu-id="8985e-103">Получает учетные записи автоматизации в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8985e-103">Gets Automation accounts in a resource group.</span></span>

## <span data-ttu-id="8985e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8985e-104">SYNTAX</span></span>

### <span data-ttu-id="8985e-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8985e-105">ByAll (Default)</span></span>
```
Get-AzAutomationAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8985e-106">ByAutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8985e-106">ByAutomationAccountName</span></span>
```
Get-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8985e-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8985e-107">DESCRIPTION</span></span>
<span data-ttu-id="8985e-108">Для получения учетных записей автоматизации Azure в группе ресурсов возвращается **cmdlet Get-AzAutomationAccount.**</span><span class="sxs-lookup"><span data-stu-id="8985e-108">The **Get-AzAutomationAccount** cmdlet gets Azure Automation accounts in a resource group.</span></span>
<span data-ttu-id="8985e-109">Дополнительные сведения об учетных записях автоматизации см. в New-AzAutomationAccount>.</span><span class="sxs-lookup"><span data-stu-id="8985e-109">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="8985e-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8985e-110">EXAMPLES</span></span>

### <span data-ttu-id="8985e-111">Пример 1. Получить все учетные записи</span><span class="sxs-lookup"><span data-stu-id="8985e-111">Example 1: Get all accounts</span></span>
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="8985e-112">Эта команда получает все учетные записи автоматизации в группе ресурсов ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="8985e-112">This command gets all Automation accounts in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="8985e-113">Пример 2. Получить учетную запись</span><span class="sxs-lookup"><span data-stu-id="8985e-113">Example 2: Get an account</span></span>
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03" -Name "ContosoAutomationAccount"
```

<span data-ttu-id="8985e-114">Эта команда получает учетную запись автоматизации ContosoAutomationAccount в группе ресурсов ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8985e-114">This command gets the Automation account named ContosoAutomationAccount in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="8985e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8985e-115">PARAMETERS</span></span>

### <span data-ttu-id="8985e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8985e-116">-DefaultProfile</span></span>
<span data-ttu-id="8985e-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8985e-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8985e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="8985e-118">-Name</span></span>
<span data-ttu-id="8985e-119">Указывает имя учетной записи автоматизации, которую получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8985e-119">Specifies the name of the Automation account that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8985e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8985e-120">-ResourceGroupName</span></span>
<span data-ttu-id="8985e-121">Указывает имя группы ресурсов, в которой этот cmdlet получает учетные записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="8985e-121">Specifies the name of a resource group in which this cmdlet gets Automation accounts.</span></span>

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

### <span data-ttu-id="8985e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8985e-122">CommonParameters</span></span>
<span data-ttu-id="8985e-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8985e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8985e-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8985e-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8985e-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8985e-125">INPUTS</span></span>

### <span data-ttu-id="8985e-126">System.String</span><span class="sxs-lookup"><span data-stu-id="8985e-126">System.String</span></span>

## <span data-ttu-id="8985e-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8985e-127">OUTPUTS</span></span>

### <span data-ttu-id="8985e-128">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8985e-128">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="8985e-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8985e-129">NOTES</span></span>

## <span data-ttu-id="8985e-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8985e-130">RELATED LINKS</span></span>

[<span data-ttu-id="8985e-131">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8985e-131">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="8985e-132">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8985e-132">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)

[<span data-ttu-id="8985e-133">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8985e-133">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)


