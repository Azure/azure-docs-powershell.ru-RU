---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 89F604DD-EE77-440D-BCC9-3F74D994C447
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
ms.openlocfilehash: ae67aac391f2cce2a37be8a5a15a0fd0ea37cdd9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411503"
---
# <span data-ttu-id="d3a10-101">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="d3a10-101">Remove-AzBatchAccount</span></span>

## <span data-ttu-id="d3a10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3a10-102">SYNOPSIS</span></span>
<span data-ttu-id="d3a10-103">Удаляет пакетную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="d3a10-103">Removes a Batch account.</span></span>

## <span data-ttu-id="d3a10-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d3a10-104">SYNTAX</span></span>

```
Remove-AzBatchAccount [-AccountName] <String> [[-ResourceGroupName] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3a10-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3a10-105">DESCRIPTION</span></span>
<span data-ttu-id="d3a10-106">С **его использованием удаляется** учетная запись Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="d3a10-106">The **Remove-AzBatchAccount** cmdlet removes an Azure Batch account.</span></span>
<span data-ttu-id="d3a10-107">При этом будет предложено удалить учетную запись, если не указан параметр *Force.*</span><span class="sxs-lookup"><span data-stu-id="d3a10-107">This cmdlet prompts you before it removes an account, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="d3a10-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d3a10-108">EXAMPLES</span></span>

### <span data-ttu-id="d3a10-109">Пример 1. Удаление учетной записи пакета</span><span class="sxs-lookup"><span data-stu-id="d3a10-109">Example 1: Remove a Batch account</span></span>
```
PS C:\>Remove-AzBatchAccount -AccountName "pfuller"
```

<span data-ttu-id="d3a10-110">Эта команда удаляет пакетную учетную запись с именем pfuller.</span><span class="sxs-lookup"><span data-stu-id="d3a10-110">This command removes the Batch account named pfuller.</span></span>
<span data-ttu-id="d3a10-111">Эта команда запросит подтверждение перед удалением учетной записи.</span><span class="sxs-lookup"><span data-stu-id="d3a10-111">This command prompts you for confirmation before it deletes the account.</span></span>

## <span data-ttu-id="d3a10-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3a10-112">PARAMETERS</span></span>

### <span data-ttu-id="d3a10-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d3a10-113">-AccountName</span></span>
<span data-ttu-id="d3a10-114">Имя учетной записи пакета, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3a10-114">Specifies the name of the Batch account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d3a10-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3a10-115">-DefaultProfile</span></span>
<span data-ttu-id="d3a10-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d3a10-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3a10-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d3a10-117">-Force</span></span>
<span data-ttu-id="d3a10-118">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="d3a10-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d3a10-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3a10-119">-ResourceGroupName</span></span>
<span data-ttu-id="d3a10-120">Определяет группу ресурсов учетной записи, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3a10-120">Specifies the resource group of the account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d3a10-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3a10-121">-Confirm</span></span>
<span data-ttu-id="d3a10-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d3a10-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3a10-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3a10-123">-WhatIf</span></span>
<span data-ttu-id="d3a10-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3a10-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3a10-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d3a10-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3a10-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3a10-126">CommonParameters</span></span>
<span data-ttu-id="d3a10-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3a10-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3a10-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3a10-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3a10-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d3a10-129">INPUTS</span></span>

### <span data-ttu-id="d3a10-130">System.String</span><span class="sxs-lookup"><span data-stu-id="d3a10-130">System.String</span></span>

## <span data-ttu-id="d3a10-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d3a10-131">OUTPUTS</span></span>

### <span data-ttu-id="d3a10-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="d3a10-132">System.Void</span></span>

## <span data-ttu-id="d3a10-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d3a10-133">NOTES</span></span>

## <span data-ttu-id="d3a10-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d3a10-134">RELATED LINKS</span></span>

[<span data-ttu-id="d3a10-135">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="d3a10-135">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="d3a10-136">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="d3a10-136">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="d3a10-137">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="d3a10-137">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="d3a10-138">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="d3a10-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
