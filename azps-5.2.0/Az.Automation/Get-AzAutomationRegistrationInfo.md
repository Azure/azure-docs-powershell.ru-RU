---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 09823BE3-A98B-42EF-B6F4-99F95F2B342E
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
ms.openlocfilehash: 226791db9057fe0f8aa246fab546dd4af7303529
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98418676"
---
# <span data-ttu-id="add81-101">Get-AzAutomationRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="add81-101">Get-AzAutomationRegistrationInfo</span></span>

## <span data-ttu-id="add81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="add81-102">SYNOPSIS</span></span>
<span data-ttu-id="add81-103">Возвращает сведения о регистрации узла DSC или гибридного сотрудника в автоматизацию.</span><span class="sxs-lookup"><span data-stu-id="add81-103">Gets registration information for onboarding a DSC node or hybrid worker to Automation.</span></span>

## <span data-ttu-id="add81-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="add81-104">SYNTAX</span></span>

```
Get-AzAutomationRegistrationInfo [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="add81-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="add81-105">DESCRIPTION</span></span>
<span data-ttu-id="add81-106">Cmdlet **Get-AzAutomationRegistrationInfo** получает конечную точку и ключи, необходимые для регистрации узла DSC или гибридного сотрудника в учетной записи автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="add81-106">The **Get-AzAutomationRegistrationInfo** cmdlet gets the endpoint and keys required to onboard a Desired State Configuration (DSC) node or hybrid worker into an Azure Automation account.</span></span>

## <span data-ttu-id="add81-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="add81-107">EXAMPLES</span></span>

### <span data-ttu-id="add81-108">Пример 1. Получить сведения о регистрации</span><span class="sxs-lookup"><span data-stu-id="add81-108">Example 1: Get registration information</span></span>
```
PS C:\>Get-AzAutomationRegistrationInfo -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="add81-109">Эта команда получает сведения о регистрации для учетной записи автоматизации AutomationAccount01 в группе ресурсов "Группа ресурсов01".</span><span class="sxs-lookup"><span data-stu-id="add81-109">This command gets the registration information for the Automation account named AutomationAccount01 in the Resource Group named ResourceGroup01.</span></span>

## <span data-ttu-id="add81-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="add81-110">PARAMETERS</span></span>

### <span data-ttu-id="add81-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="add81-111">-AutomationAccountName</span></span>
<span data-ttu-id="add81-112">Указывает имя учетной записи автоматизации, для которой этот cmdlet получает сведения о регистрации.</span><span class="sxs-lookup"><span data-stu-id="add81-112">Specifies the name of Automation account for which this cmdlet gets registration information.</span></span>

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

### <span data-ttu-id="add81-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="add81-113">-DefaultProfile</span></span>
<span data-ttu-id="add81-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="add81-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="add81-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="add81-115">-ResourceGroupName</span></span>
<span data-ttu-id="add81-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="add81-116">Specifies the name of a resource group.</span></span>
<span data-ttu-id="add81-117">Этот cmdlet получает сведения о регистрации для группы ресурсов, заданной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="add81-117">This cmdlet gets registration information for the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="add81-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="add81-118">CommonParameters</span></span>
<span data-ttu-id="add81-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="add81-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="add81-120">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="add81-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="add81-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="add81-121">INPUTS</span></span>

### <span data-ttu-id="add81-122">System.String</span><span class="sxs-lookup"><span data-stu-id="add81-122">System.String</span></span>

## <span data-ttu-id="add81-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="add81-123">OUTPUTS</span></span>

### <span data-ttu-id="add81-124">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="add81-124">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="add81-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="add81-125">NOTES</span></span>

## <span data-ttu-id="add81-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="add81-126">RELATED LINKS</span></span>

[<span data-ttu-id="add81-127">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="add81-127">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="add81-128">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="add81-128">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="add81-129">New-AzAutomationKey</span><span class="sxs-lookup"><span data-stu-id="add81-129">New-AzAutomationKey</span></span>](./New-AzAutomationKey.md)


