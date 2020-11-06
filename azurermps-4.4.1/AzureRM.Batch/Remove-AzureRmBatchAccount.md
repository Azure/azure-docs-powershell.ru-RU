---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 89F604DD-EE77-440D-BCC9-3F74D994C447
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchAccount.md
ms.openlocfilehash: 3de75d2c8e7ed69a8f5be02833dd002ee5fbf016
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566757"
---
# <span data-ttu-id="63638-101">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="63638-101">Remove-AzureRmBatchAccount</span></span>

## <span data-ttu-id="63638-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="63638-102">SYNOPSIS</span></span>
<span data-ttu-id="63638-103">Удаляет пакетную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="63638-103">Removes a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63638-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="63638-104">SYNTAX</span></span>

```
Remove-AzureRmBatchAccount [-AccountName] <String> [[-ResourceGroupName] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63638-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="63638-105">DESCRIPTION</span></span>
<span data-ttu-id="63638-106">Командлет **Remove-AzureRmBatchAccount** удаляет пакетную учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="63638-106">The **Remove-AzureRmBatchAccount** cmdlet removes an Azure Batch account.</span></span>
<span data-ttu-id="63638-107">Этот командлет предложит вам перед удалением учетной записи, если не указан параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="63638-107">This cmdlet prompts you before it removes an account, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="63638-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="63638-108">EXAMPLES</span></span>

### <span data-ttu-id="63638-109">Пример 1: Удаление учетной записи пакета</span><span class="sxs-lookup"><span data-stu-id="63638-109">Example 1: Remove a Batch account</span></span>
```
PS C:\>Remove-AzureRmBatchAccount -AccountName "pfuller"
```

<span data-ttu-id="63638-110">Эта команда удаляет пакетную учетную запись с именем pfuller.</span><span class="sxs-lookup"><span data-stu-id="63638-110">This command removes the Batch account named pfuller.</span></span>
<span data-ttu-id="63638-111">Эта команда запрашивает подтверждение перед удалением учетной записи.</span><span class="sxs-lookup"><span data-stu-id="63638-111">This command prompts you for confirmation before it deletes the account.</span></span>

## <span data-ttu-id="63638-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="63638-112">PARAMETERS</span></span>

### <span data-ttu-id="63638-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="63638-113">-AccountName</span></span>
<span data-ttu-id="63638-114">Указывает имя пакетной учетной записи, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="63638-114">Specifies the name of the Batch account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="63638-115">-Force</span><span class="sxs-lookup"><span data-stu-id="63638-115">-Force</span></span>
<span data-ttu-id="63638-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="63638-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="63638-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63638-117">-ResourceGroupName</span></span>
<span data-ttu-id="63638-118">Указывает группу ресурсов для учетной записи, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="63638-118">Specifies the resource group of the account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="63638-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="63638-119">-Confirm</span></span>
<span data-ttu-id="63638-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="63638-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63638-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63638-121">-WhatIf</span></span>
<span data-ttu-id="63638-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="63638-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63638-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="63638-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63638-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63638-124">-DefaultProfile</span></span>
<span data-ttu-id="63638-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="63638-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63638-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63638-126">CommonParameters</span></span>
<span data-ttu-id="63638-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="63638-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63638-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63638-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63638-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="63638-129">INPUTS</span></span>

## <span data-ttu-id="63638-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="63638-130">OUTPUTS</span></span>

## <span data-ttu-id="63638-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="63638-131">NOTES</span></span>

## <span data-ttu-id="63638-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63638-132">RELATED LINKS</span></span>

[<span data-ttu-id="63638-133">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="63638-133">Get-AzureRmBatchAccount</span></span>](./Get-AzureRmBatchAccount.md)

[<span data-ttu-id="63638-134">New-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="63638-134">New-AzureRmBatchAccount</span></span>](./New-AzureRmBatchAccount.md)

[<span data-ttu-id="63638-135">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="63638-135">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="63638-136">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="63638-136">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


