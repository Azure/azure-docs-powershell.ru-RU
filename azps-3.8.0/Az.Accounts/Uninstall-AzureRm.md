---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/uninstall-azurerm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
ms.openlocfilehash: ee581528810663d09fe724f370b681ff9e20072f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066457"
---
# <span data-ttu-id="4bb25-101">Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="4bb25-101">Uninstall-AzureRm</span></span>

## <span data-ttu-id="4bb25-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4bb25-102">SYNOPSIS</span></span>
<span data-ttu-id="4bb25-103">Удаление всех AzureRmных модулей с компьютера.</span><span class="sxs-lookup"><span data-stu-id="4bb25-103">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="4bb25-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4bb25-104">SYNTAX</span></span>

```
Uninstall-AzureRm [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4bb25-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4bb25-105">DESCRIPTION</span></span>
<span data-ttu-id="4bb25-106">Удаление всех AzureRmных модулей с компьютера.</span><span class="sxs-lookup"><span data-stu-id="4bb25-106">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="4bb25-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4bb25-107">EXAMPLES</span></span>

### <span data-ttu-id="4bb25-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4bb25-108">Example 1</span></span>
```
PS C:\> Uninstall-AzureRm
```

<span data-ttu-id="4bb25-109">Выполнение этой команды приведет к удалению всех модулей AzureRm с компьютера для версии PowerShell, в которой выполняется командлет.</span><span class="sxs-lookup"><span data-stu-id="4bb25-109">Running this command will remove all AzureRm modules from the machine for the version of PowerShell in which the cmdlet is run.</span></span>

## <span data-ttu-id="4bb25-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4bb25-110">PARAMETERS</span></span>

### <span data-ttu-id="4bb25-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bb25-111">-DefaultProfile</span></span>
<span data-ttu-id="4bb25-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4bb25-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bb25-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4bb25-113">-PassThru</span></span>
<span data-ttu-id="4bb25-114">Возвращает список модулей, которые удалены, если они указаны.</span><span class="sxs-lookup"><span data-stu-id="4bb25-114">Return list of Modules removed if specified.</span></span>

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

### <span data-ttu-id="4bb25-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4bb25-115">-Confirm</span></span>
<span data-ttu-id="4bb25-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4bb25-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bb25-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bb25-117">-WhatIf</span></span>
<span data-ttu-id="4bb25-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4bb25-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bb25-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4bb25-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bb25-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bb25-120">CommonParameters</span></span>
<span data-ttu-id="4bb25-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4bb25-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bb25-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bb25-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bb25-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4bb25-123">INPUTS</span></span>

### <span data-ttu-id="4bb25-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="4bb25-124">None</span></span>

## <span data-ttu-id="4bb25-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4bb25-125">OUTPUTS</span></span>

### <span data-ttu-id="4bb25-126">System. String</span><span class="sxs-lookup"><span data-stu-id="4bb25-126">System.String</span></span>

## <span data-ttu-id="4bb25-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="4bb25-127">NOTES</span></span>

## <span data-ttu-id="4bb25-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4bb25-128">RELATED LINKS</span></span>
