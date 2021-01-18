---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/uninstall-azurerm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
ms.openlocfilehash: ee581528810663d09fe724f370b681ff9e20072f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507002"
---
# <span data-ttu-id="995d3-101">Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="995d3-101">Uninstall-AzureRm</span></span>

## <span data-ttu-id="995d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="995d3-102">SYNOPSIS</span></span>
<span data-ttu-id="995d3-103">Удаляет все модули AzureRm с компьютера.</span><span class="sxs-lookup"><span data-stu-id="995d3-103">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="995d3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="995d3-104">SYNTAX</span></span>

```
Uninstall-AzureRm [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="995d3-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="995d3-105">DESCRIPTION</span></span>
<span data-ttu-id="995d3-106">Удаляет все модули AzureRm с компьютера.</span><span class="sxs-lookup"><span data-stu-id="995d3-106">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="995d3-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="995d3-107">EXAMPLES</span></span>

### <span data-ttu-id="995d3-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="995d3-108">Example 1</span></span>
```
PS C:\> Uninstall-AzureRm
```

<span data-ttu-id="995d3-109">Эта команда удаляет с компьютера все модули AzureRm для версии PowerShell, в которой запущен командлет.</span><span class="sxs-lookup"><span data-stu-id="995d3-109">Running this command will remove all AzureRm modules from the machine for the version of PowerShell in which the cmdlet is run.</span></span>

## <span data-ttu-id="995d3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="995d3-110">PARAMETERS</span></span>

### <span data-ttu-id="995d3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="995d3-111">-DefaultProfile</span></span>
<span data-ttu-id="995d3-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="995d3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="995d3-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="995d3-113">-PassThru</span></span>
<span data-ttu-id="995d3-114">Список возвратов модулей, если заданный, удаляется.</span><span class="sxs-lookup"><span data-stu-id="995d3-114">Return list of Modules removed if specified.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="995d3-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="995d3-115">-Confirm</span></span>
<span data-ttu-id="995d3-116">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="995d3-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="995d3-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="995d3-117">-WhatIf</span></span>
<span data-ttu-id="995d3-118">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="995d3-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="995d3-119">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="995d3-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="995d3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="995d3-120">CommonParameters</span></span>
<span data-ttu-id="995d3-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="995d3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="995d3-122">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="995d3-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="995d3-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="995d3-123">INPUTS</span></span>

### <span data-ttu-id="995d3-124">Нет</span><span class="sxs-lookup"><span data-stu-id="995d3-124">None</span></span>

## <span data-ttu-id="995d3-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="995d3-125">OUTPUTS</span></span>

### <span data-ttu-id="995d3-126">System.String</span><span class="sxs-lookup"><span data-stu-id="995d3-126">System.String</span></span>

## <span data-ttu-id="995d3-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="995d3-127">NOTES</span></span>

## <span data-ttu-id="995d3-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="995d3-128">RELATED LINKS</span></span>
