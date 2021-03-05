---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/uninstall-azurerm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
ms.openlocfilehash: 796690bd0a5774e488b978003c48b02eedaac190
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967091"
---
# <span data-ttu-id="0fccb-101">Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="0fccb-101">Uninstall-AzureRm</span></span>

## <span data-ttu-id="0fccb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fccb-102">SYNOPSIS</span></span>
<span data-ttu-id="0fccb-103">Удаляет все модули AzureRm с компьютера.</span><span class="sxs-lookup"><span data-stu-id="0fccb-103">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="0fccb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0fccb-104">SYNTAX</span></span>

```
Uninstall-AzureRm [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0fccb-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0fccb-105">DESCRIPTION</span></span>
<span data-ttu-id="0fccb-106">Удаляет все модули AzureRm с компьютера.</span><span class="sxs-lookup"><span data-stu-id="0fccb-106">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="0fccb-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0fccb-107">EXAMPLES</span></span>

### <span data-ttu-id="0fccb-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0fccb-108">Example 1</span></span>
```
PS C:\> Uninstall-AzureRm
```

<span data-ttu-id="0fccb-109">Эта команда удаляет с компьютера все модули AzureRm для версии PowerShell, в которой запущен командлет.</span><span class="sxs-lookup"><span data-stu-id="0fccb-109">Running this command will remove all AzureRm modules from the machine for the version of PowerShell in which the cmdlet is run.</span></span>

## <span data-ttu-id="0fccb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0fccb-110">PARAMETERS</span></span>

### <span data-ttu-id="0fccb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fccb-111">-DefaultProfile</span></span>
<span data-ttu-id="0fccb-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0fccb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fccb-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0fccb-113">-PassThru</span></span>
<span data-ttu-id="0fccb-114">Список возвратов модулей, если заданный, удаляется.</span><span class="sxs-lookup"><span data-stu-id="0fccb-114">Return list of Modules removed if specified.</span></span>

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

### <span data-ttu-id="0fccb-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0fccb-115">-Confirm</span></span>
<span data-ttu-id="0fccb-116">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0fccb-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fccb-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fccb-117">-WhatIf</span></span>
<span data-ttu-id="0fccb-118">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0fccb-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fccb-119">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0fccb-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fccb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fccb-120">CommonParameters</span></span>
<span data-ttu-id="0fccb-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fccb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fccb-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0fccb-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fccb-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0fccb-123">INPUTS</span></span>

### <span data-ttu-id="0fccb-124">Нет</span><span class="sxs-lookup"><span data-stu-id="0fccb-124">None</span></span>

## <span data-ttu-id="0fccb-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0fccb-125">OUTPUTS</span></span>

### <span data-ttu-id="0fccb-126">System.String</span><span class="sxs-lookup"><span data-stu-id="0fccb-126">System.String</span></span>

## <span data-ttu-id="0fccb-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0fccb-127">NOTES</span></span>

## <span data-ttu-id="0fccb-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0fccb-128">RELATED LINKS</span></span>
