---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 89F604DD-EE77-440D-BCC9-3F74D994C447
online version: https://docs.microsoft.com/powershell/module/az.batch/remove-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
ms.openlocfilehash: 5b74f378bc867c1d39f27ebdd9972dfdda5457c2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007331"
---
# <span data-ttu-id="6f62f-101">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="6f62f-101">Remove-AzBatchAccount</span></span>

## <span data-ttu-id="6f62f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f62f-102">SYNOPSIS</span></span>
<span data-ttu-id="6f62f-103">Удаляет учетную запись пакета.</span><span class="sxs-lookup"><span data-stu-id="6f62f-103">Removes a Batch account.</span></span>

## <span data-ttu-id="6f62f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6f62f-104">SYNTAX</span></span>

```
Remove-AzBatchAccount [-AccountName] <String> [[-ResourceGroupName] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f62f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f62f-105">DESCRIPTION</span></span>
<span data-ttu-id="6f62f-106">С **его использованием удаляется** учетная запись Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="6f62f-106">The **Remove-AzBatchAccount** cmdlet removes an Azure Batch account.</span></span>
<span data-ttu-id="6f62f-107">При этом будет предложено удалить учетную запись, если не указан параметр *Force.*</span><span class="sxs-lookup"><span data-stu-id="6f62f-107">This cmdlet prompts you before it removes an account, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="6f62f-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6f62f-108">EXAMPLES</span></span>

### <span data-ttu-id="6f62f-109">Пример 1. Удаление учетной записи пакета</span><span class="sxs-lookup"><span data-stu-id="6f62f-109">Example 1: Remove a Batch account</span></span>
```
PS C:\>Remove-AzBatchAccount -AccountName "pfuller"
```

<span data-ttu-id="6f62f-110">Эта команда удаляет пакетную учетную запись с именем pfuller.</span><span class="sxs-lookup"><span data-stu-id="6f62f-110">This command removes the Batch account named pfuller.</span></span>
<span data-ttu-id="6f62f-111">Эта команда запросит подтверждение перед удалением учетной записи.</span><span class="sxs-lookup"><span data-stu-id="6f62f-111">This command prompts you for confirmation before it deletes the account.</span></span>

## <span data-ttu-id="6f62f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f62f-112">PARAMETERS</span></span>

### <span data-ttu-id="6f62f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6f62f-113">-AccountName</span></span>
<span data-ttu-id="6f62f-114">Имя учетной записи пакета, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f62f-114">Specifies the name of the Batch account that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f62f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f62f-115">-DefaultProfile</span></span>
<span data-ttu-id="6f62f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6f62f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f62f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6f62f-117">-Force</span></span>
<span data-ttu-id="6f62f-118">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="6f62f-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6f62f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f62f-119">-ResourceGroupName</span></span>
<span data-ttu-id="6f62f-120">Определяет группу ресурсов учетной записи, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f62f-120">Specifies the resource group of the account that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f62f-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6f62f-121">-Confirm</span></span>
<span data-ttu-id="6f62f-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="6f62f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f62f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f62f-123">-WhatIf</span></span>
<span data-ttu-id="6f62f-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f62f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f62f-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6f62f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f62f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f62f-126">CommonParameters</span></span>
<span data-ttu-id="6f62f-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f62f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f62f-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6f62f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f62f-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6f62f-129">INPUTS</span></span>

### <span data-ttu-id="6f62f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="6f62f-130">System.String</span></span>

## <span data-ttu-id="6f62f-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6f62f-131">OUTPUTS</span></span>

### <span data-ttu-id="6f62f-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="6f62f-132">System.Void</span></span>

## <span data-ttu-id="6f62f-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6f62f-133">NOTES</span></span>

## <span data-ttu-id="6f62f-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6f62f-134">RELATED LINKS</span></span>

[<span data-ttu-id="6f62f-135">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="6f62f-135">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="6f62f-136">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="6f62f-136">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="6f62f-137">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="6f62f-137">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="6f62f-138">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="6f62f-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
