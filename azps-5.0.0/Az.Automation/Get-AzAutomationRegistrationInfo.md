---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 09823BE3-A98B-42EF-B6F4-99F95F2B342E
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
ms.openlocfilehash: 226791db9057fe0f8aa246fab546dd4af7303529
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248136"
---
# <span data-ttu-id="4ab2c-101">Get-AzAutomationRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="4ab2c-101">Get-AzAutomationRegistrationInfo</span></span>

## <span data-ttu-id="4ab2c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4ab2c-102">SYNOPSIS</span></span>
<span data-ttu-id="4ab2c-103">Получение сведений о регистрации для настольных систем DSC или гибридных рабочих процессов для автоматизации.</span><span class="sxs-lookup"><span data-stu-id="4ab2c-103">Gets registration information for onboarding a DSC node or hybrid worker to Automation.</span></span>

## <span data-ttu-id="4ab2c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4ab2c-104">SYNTAX</span></span>

```
Get-AzAutomationRegistrationInfo [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ab2c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ab2c-105">DESCRIPTION</span></span>
<span data-ttu-id="4ab2c-106">Командлет **Get-AzAutomationRegistrationInfo** получает конечную точку и ключи, необходимые для встроенного узла конфигурации (DSC) или гибридного рабочего процесса в учетную запись службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="4ab2c-106">The **Get-AzAutomationRegistrationInfo** cmdlet gets the endpoint and keys required to onboard a Desired State Configuration (DSC) node or hybrid worker into an Azure Automation account.</span></span>

## <span data-ttu-id="4ab2c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4ab2c-107">EXAMPLES</span></span>

### <span data-ttu-id="4ab2c-108">Пример 1: получение регистрационных данных</span><span class="sxs-lookup"><span data-stu-id="4ab2c-108">Example 1: Get registration information</span></span>
```
PS C:\>Get-AzAutomationRegistrationInfo -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="4ab2c-109">Эта команда получает регистрационные данные для учетной записи автоматизации с именем AutomationAccount01 в группе ресурсов с именем ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="4ab2c-109">This command gets the registration information for the Automation account named AutomationAccount01 in the Resource Group named ResourceGroup01.</span></span>

## <span data-ttu-id="4ab2c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4ab2c-110">PARAMETERS</span></span>

### <span data-ttu-id="4ab2c-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4ab2c-111">-AutomationAccountName</span></span>
<span data-ttu-id="4ab2c-112">Указывает имя учетной записи автоматизации, для которой этот командлет получает сведения о регистрации.</span><span class="sxs-lookup"><span data-stu-id="4ab2c-112">Specifies the name of Automation account for which this cmdlet gets registration information.</span></span>

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

### <span data-ttu-id="4ab2c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ab2c-113">-DefaultProfile</span></span>
<span data-ttu-id="4ab2c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4ab2c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ab2c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ab2c-115">-ResourceGroupName</span></span>
<span data-ttu-id="4ab2c-116">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4ab2c-116">Specifies the name of a resource group.</span></span>
<span data-ttu-id="4ab2c-117">Этот командлет получает регистрационные данные для группы ресурсов, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="4ab2c-117">This cmdlet gets registration information for the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="4ab2c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ab2c-118">CommonParameters</span></span>
<span data-ttu-id="4ab2c-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4ab2c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ab2c-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ab2c-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ab2c-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4ab2c-121">INPUTS</span></span>

### <span data-ttu-id="4ab2c-122">System. String</span><span class="sxs-lookup"><span data-stu-id="4ab2c-122">System.String</span></span>

## <span data-ttu-id="4ab2c-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ab2c-123">OUTPUTS</span></span>

### <span data-ttu-id="4ab2c-124">Microsoft. Azure. Commands. Automation. Model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="4ab2c-124">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="4ab2c-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="4ab2c-125">NOTES</span></span>

## <span data-ttu-id="4ab2c-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4ab2c-126">RELATED LINKS</span></span>

[<span data-ttu-id="4ab2c-127">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="4ab2c-127">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="4ab2c-128">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="4ab2c-128">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="4ab2c-129">New-AzAutomationKey</span><span class="sxs-lookup"><span data-stu-id="4ab2c-129">New-AzAutomationKey</span></span>](./New-AzAutomationKey.md)

