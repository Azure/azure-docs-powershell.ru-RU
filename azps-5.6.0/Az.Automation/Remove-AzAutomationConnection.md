---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C1C0F69D-6A3F-4523-BB70-27676A3DDCBD
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
ms.openlocfilehash: 0534f05bcc59a109851188c8b585badfc90d61c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009971"
---
# <span data-ttu-id="63d2b-101">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="63d2b-101">Remove-AzAutomationConnection</span></span>

## <span data-ttu-id="63d2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63d2b-102">SYNOPSIS</span></span>
<span data-ttu-id="63d2b-103">Удаляет соединение автоматизации.</span><span class="sxs-lookup"><span data-stu-id="63d2b-103">Removes an Automation connection.</span></span>

## <span data-ttu-id="63d2b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="63d2b-104">SYNTAX</span></span>

```
Remove-AzAutomationConnection [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="63d2b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="63d2b-105">DESCRIPTION</span></span>
<span data-ttu-id="63d2b-106">Для удаления соединения из автоматизации Azure удаляется **cmdlet Remove-AzAutomationConnection.**</span><span class="sxs-lookup"><span data-stu-id="63d2b-106">The **Remove-AzAutomationConnection** cmdlet removes a connection from Azure Automation.</span></span>

## <span data-ttu-id="63d2b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="63d2b-107">EXAMPLES</span></span>

### <span data-ttu-id="63d2b-108">Пример 1. Удаление подключения</span><span class="sxs-lookup"><span data-stu-id="63d2b-108">Example 1: Remove a connection</span></span>
```
PS C:\>Remove-AzAutomationConnection -AutomationAccountName "Contoso17" -Name "ContosoConnection" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="63d2b-109">Эта команда удаляет сертификат ContosoConnection в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="63d2b-109">This command removes a certificate named ContosoConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="63d2b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63d2b-110">PARAMETERS</span></span>

### <span data-ttu-id="63d2b-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="63d2b-111">-AutomationAccountName</span></span>
<span data-ttu-id="63d2b-112">Указывает имя учетной записи автоматизации, для которой этот cmdlet удаляет подключение.</span><span class="sxs-lookup"><span data-stu-id="63d2b-112">Specifies the name of the automation account for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="63d2b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63d2b-113">-DefaultProfile</span></span>
<span data-ttu-id="63d2b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="63d2b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="63d2b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="63d2b-115">-Force</span></span>
<span data-ttu-id="63d2b-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="63d2b-116">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63d2b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="63d2b-117">-Name</span></span>
<span data-ttu-id="63d2b-118">Указывает имя подключения, которое удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63d2b-118">Specifies the name of the connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="63d2b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63d2b-119">-ResourceGroupName</span></span>
<span data-ttu-id="63d2b-120">Имя группы ресурсов, для которой этот cmdlet удаляет подключение.</span><span class="sxs-lookup"><span data-stu-id="63d2b-120">Specifies the name of the resource group for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="63d2b-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="63d2b-121">-Confirm</span></span>
<span data-ttu-id="63d2b-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63d2b-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63d2b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63d2b-123">-WhatIf</span></span>
<span data-ttu-id="63d2b-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63d2b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63d2b-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="63d2b-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63d2b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63d2b-126">CommonParameters</span></span>
<span data-ttu-id="63d2b-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63d2b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63d2b-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63d2b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63d2b-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="63d2b-129">INPUTS</span></span>

### <span data-ttu-id="63d2b-130">System.String</span><span class="sxs-lookup"><span data-stu-id="63d2b-130">System.String</span></span>

## <span data-ttu-id="63d2b-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="63d2b-131">OUTPUTS</span></span>

### <span data-ttu-id="63d2b-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="63d2b-132">System.Void</span></span>

## <span data-ttu-id="63d2b-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="63d2b-133">NOTES</span></span>

## <span data-ttu-id="63d2b-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63d2b-134">RELATED LINKS</span></span>

[<span data-ttu-id="63d2b-135">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="63d2b-135">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="63d2b-136">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="63d2b-136">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)


