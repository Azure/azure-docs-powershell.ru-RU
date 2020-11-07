---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/uninstall-azurerm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
ms.openlocfilehash: d2e495b58e68232bf20bd309d06207cd45cd427e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728222"
---
# <span data-ttu-id="caa93-101">Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="caa93-101">Uninstall-AzureRm</span></span>

## <span data-ttu-id="caa93-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="caa93-102">SYNOPSIS</span></span>
<span data-ttu-id="caa93-103">Удаление всех AzureRmных модулей с компьютера.</span><span class="sxs-lookup"><span data-stu-id="caa93-103">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="caa93-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="caa93-104">SYNTAX</span></span>

```
Uninstall-AzureRm [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="caa93-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="caa93-105">DESCRIPTION</span></span>
<span data-ttu-id="caa93-106">Удаление всех AzureRmных модулей с компьютера.</span><span class="sxs-lookup"><span data-stu-id="caa93-106">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="caa93-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="caa93-107">EXAMPLES</span></span>

### <span data-ttu-id="caa93-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="caa93-108">Example 1</span></span>
```
PS C:\> Uninstall-AzureRm
```

<span data-ttu-id="caa93-109">Выполнение этой команды приведет к удалению всех модулей AzureRm с компьютера для версии PowerShell, в которой выполняется командлет.</span><span class="sxs-lookup"><span data-stu-id="caa93-109">Running this command will remove all AzureRm modules from the machine for the version of PowerShell in which the cmdlet is run.</span></span>

## <span data-ttu-id="caa93-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="caa93-110">PARAMETERS</span></span>

### <span data-ttu-id="caa93-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caa93-111">-DefaultProfile</span></span>
<span data-ttu-id="caa93-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="caa93-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="caa93-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="caa93-113">-PassThru</span></span>
<span data-ttu-id="caa93-114">Возвращает список модулей, которые удалены, если они указаны.</span><span class="sxs-lookup"><span data-stu-id="caa93-114">Return list of Modules removed if specified.</span></span>

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

### <span data-ttu-id="caa93-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="caa93-115">-Confirm</span></span>
<span data-ttu-id="caa93-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="caa93-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="caa93-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="caa93-117">-WhatIf</span></span>
<span data-ttu-id="caa93-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="caa93-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="caa93-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="caa93-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="caa93-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caa93-120">CommonParameters</span></span>
<span data-ttu-id="caa93-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="caa93-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caa93-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="caa93-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caa93-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="caa93-123">INPUTS</span></span>

### <span data-ttu-id="caa93-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="caa93-124">None</span></span>

## <span data-ttu-id="caa93-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="caa93-125">OUTPUTS</span></span>

### <span data-ttu-id="caa93-126">System. String</span><span class="sxs-lookup"><span data-stu-id="caa93-126">System.String</span></span>

## <span data-ttu-id="caa93-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="caa93-127">NOTES</span></span>

## <span data-ttu-id="caa93-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="caa93-128">RELATED LINKS</span></span>
