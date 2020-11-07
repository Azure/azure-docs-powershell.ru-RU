---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 09823BE3-A98B-42EF-B6F4-99F95F2B342E
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
ms.openlocfilehash: f915d1637226e7381cf7da53c0a3aea022060be1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727839"
---
# <span data-ttu-id="6e738-101">Get-AzAutomationRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="6e738-101">Get-AzAutomationRegistrationInfo</span></span>

## <span data-ttu-id="6e738-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6e738-102">SYNOPSIS</span></span>
<span data-ttu-id="6e738-103">Получение сведений о регистрации для настольных систем DSC или гибридных рабочих процессов для автоматизации.</span><span class="sxs-lookup"><span data-stu-id="6e738-103">Gets registration information for onboarding a DSC node or hybrid worker to Automation.</span></span>

## <span data-ttu-id="6e738-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6e738-104">SYNTAX</span></span>

```
Get-AzAutomationRegistrationInfo [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e738-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e738-105">DESCRIPTION</span></span>
<span data-ttu-id="6e738-106">Командлет **Get-AzAutomationRegistrationInfo** получает конечную точку и ключи, необходимые для встроенного узла конфигурации (DSC) или гибридного рабочего процесса в учетную запись службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="6e738-106">The **Get-AzAutomationRegistrationInfo** cmdlet gets the endpoint and keys required to onboard a Desired State Configuration (DSC) node or hybrid worker into an Azure Automation account.</span></span>

## <span data-ttu-id="6e738-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6e738-107">EXAMPLES</span></span>

### <span data-ttu-id="6e738-108">Пример 1: получение регистрационных данных</span><span class="sxs-lookup"><span data-stu-id="6e738-108">Example 1: Get registration information</span></span>
```
PS C:\>Get-AzAutomationRegistrationInfo -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="6e738-109">Эта команда получает регистрационные данные для учетной записи автоматизации с именем AutomationAccount01 в группе ресурсов с именем ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="6e738-109">This command gets the registration information for the Automation account named AutomationAccount01 in the Resource Group named ResourceGroup01.</span></span>

## <span data-ttu-id="6e738-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6e738-110">PARAMETERS</span></span>

### <span data-ttu-id="6e738-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6e738-111">-AutomationAccountName</span></span>
<span data-ttu-id="6e738-112">Указывает имя учетной записи автоматизации, для которой этот командлет получает сведения о регистрации.</span><span class="sxs-lookup"><span data-stu-id="6e738-112">Specifies the name of Automation account for which this cmdlet gets registration information.</span></span>

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

### <span data-ttu-id="6e738-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e738-113">-DefaultProfile</span></span>
<span data-ttu-id="6e738-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6e738-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6e738-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e738-115">-ResourceGroupName</span></span>
<span data-ttu-id="6e738-116">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6e738-116">Specifies the name of a resource group.</span></span>
<span data-ttu-id="6e738-117">Этот командлет получает регистрационные данные для группы ресурсов, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="6e738-117">This cmdlet gets registration information for the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="6e738-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e738-118">CommonParameters</span></span>
<span data-ttu-id="6e738-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6e738-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e738-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e738-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e738-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6e738-121">INPUTS</span></span>

### <span data-ttu-id="6e738-122">System. String</span><span class="sxs-lookup"><span data-stu-id="6e738-122">System.String</span></span>

## <span data-ttu-id="6e738-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e738-123">OUTPUTS</span></span>

### <span data-ttu-id="6e738-124">Microsoft. Azure. Commands. Automation. Model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="6e738-124">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="6e738-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="6e738-125">NOTES</span></span>

## <span data-ttu-id="6e738-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6e738-126">RELATED LINKS</span></span>

[<span data-ttu-id="6e738-127">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="6e738-127">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="6e738-128">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="6e738-128">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="6e738-129">New-AzAutomationKey</span><span class="sxs-lookup"><span data-stu-id="6e738-129">New-AzAutomationKey</span></span>](./New-AzAutomationKey.md)


