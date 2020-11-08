---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 89F604DD-EE77-440D-BCC9-3F74D994C447
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
ms.openlocfilehash: ae67aac391f2cce2a37be8a5a15a0fd0ea37cdd9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242598"
---
# <span data-ttu-id="89498-101">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="89498-101">Remove-AzBatchAccount</span></span>

## <span data-ttu-id="89498-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="89498-102">SYNOPSIS</span></span>
<span data-ttu-id="89498-103">Удаляет пакетную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="89498-103">Removes a Batch account.</span></span>

## <span data-ttu-id="89498-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="89498-104">SYNTAX</span></span>

```
Remove-AzBatchAccount [-AccountName] <String> [[-ResourceGroupName] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89498-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89498-105">DESCRIPTION</span></span>
<span data-ttu-id="89498-106">Командлет **Remove-AzBatchAccount** удаляет пакетную учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="89498-106">The **Remove-AzBatchAccount** cmdlet removes an Azure Batch account.</span></span>
<span data-ttu-id="89498-107">Этот командлет предложит вам перед удалением учетной записи, если не указан параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="89498-107">This cmdlet prompts you before it removes an account, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="89498-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="89498-108">EXAMPLES</span></span>

### <span data-ttu-id="89498-109">Пример 1: Удаление учетной записи пакета</span><span class="sxs-lookup"><span data-stu-id="89498-109">Example 1: Remove a Batch account</span></span>
```
PS C:\>Remove-AzBatchAccount -AccountName "pfuller"
```

<span data-ttu-id="89498-110">Эта команда удаляет пакетную учетную запись с именем pfuller.</span><span class="sxs-lookup"><span data-stu-id="89498-110">This command removes the Batch account named pfuller.</span></span>
<span data-ttu-id="89498-111">Эта команда запрашивает подтверждение перед удалением учетной записи.</span><span class="sxs-lookup"><span data-stu-id="89498-111">This command prompts you for confirmation before it deletes the account.</span></span>

## <span data-ttu-id="89498-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="89498-112">PARAMETERS</span></span>

### <span data-ttu-id="89498-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="89498-113">-AccountName</span></span>
<span data-ttu-id="89498-114">Указывает имя пакетной учетной записи, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="89498-114">Specifies the name of the Batch account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="89498-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89498-115">-DefaultProfile</span></span>
<span data-ttu-id="89498-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="89498-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89498-117">-Force</span><span class="sxs-lookup"><span data-stu-id="89498-117">-Force</span></span>
<span data-ttu-id="89498-118">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="89498-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="89498-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89498-119">-ResourceGroupName</span></span>
<span data-ttu-id="89498-120">Указывает группу ресурсов для учетной записи, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="89498-120">Specifies the resource group of the account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="89498-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="89498-121">-Confirm</span></span>
<span data-ttu-id="89498-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="89498-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89498-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89498-123">-WhatIf</span></span>
<span data-ttu-id="89498-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="89498-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89498-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="89498-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89498-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89498-126">CommonParameters</span></span>
<span data-ttu-id="89498-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="89498-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89498-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="89498-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89498-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="89498-129">INPUTS</span></span>

### <span data-ttu-id="89498-130">System. String</span><span class="sxs-lookup"><span data-stu-id="89498-130">System.String</span></span>

## <span data-ttu-id="89498-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="89498-131">OUTPUTS</span></span>

### <span data-ttu-id="89498-132">System. void</span><span class="sxs-lookup"><span data-stu-id="89498-132">System.Void</span></span>

## <span data-ttu-id="89498-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="89498-133">NOTES</span></span>

## <span data-ttu-id="89498-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89498-134">RELATED LINKS</span></span>

[<span data-ttu-id="89498-135">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="89498-135">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="89498-136">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="89498-136">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="89498-137">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="89498-137">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="89498-138">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="89498-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)