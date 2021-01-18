---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJob.md
ms.openlocfilehash: 545979c621a807c2a866fc5cf1d29aa0b659dc82
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509765"
---
# <span data-ttu-id="2a5c0-101">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2a5c0-101">Enable-AzBatchJob</span></span>

## <span data-ttu-id="2a5c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a5c0-102">SYNOPSIS</span></span>
<span data-ttu-id="2a5c0-103">Включает пакетное задание.</span><span class="sxs-lookup"><span data-stu-id="2a5c0-103">Enables a Batch job.</span></span>

## <span data-ttu-id="2a5c0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2a5c0-104">SYNTAX</span></span>

```
Enable-AzBatchJob [-Id] <String> -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2a5c0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a5c0-105">DESCRIPTION</span></span>
<span data-ttu-id="2a5c0-106">С **помощью cmdlet Enable-AzBatchJob** можно включить задание пакета Azure.</span><span class="sxs-lookup"><span data-stu-id="2a5c0-106">The **Enable-AzBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="2a5c0-107">После того как задание будет в которое в включиться, могут выполняться новые задачи.</span><span class="sxs-lookup"><span data-stu-id="2a5c0-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="2a5c0-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2a5c0-108">EXAMPLES</span></span>

### <span data-ttu-id="2a5c0-109">Пример 1. Включить пакетное задание</span><span class="sxs-lookup"><span data-stu-id="2a5c0-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="2a5c0-110">Эта команда включает задание с заданием ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="2a5c0-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="2a5c0-111">Используйте Get-AzBatchAccountKey для назначения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="2a5c0-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="2a5c0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a5c0-112">PARAMETERS</span></span>

### <span data-ttu-id="2a5c0-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="2a5c0-113">-BatchContext</span></span>
<span data-ttu-id="2a5c0-114">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="2a5c0-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2a5c0-115">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой пакета будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2a5c0-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="2a5c0-116">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="2a5c0-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="2a5c0-117">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2a5c0-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="2a5c0-118">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="2a5c0-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a5c0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a5c0-119">-DefaultProfile</span></span>
<span data-ttu-id="2a5c0-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2a5c0-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a5c0-121">-Id</span><span class="sxs-lookup"><span data-stu-id="2a5c0-121">-Id</span></span>
<span data-ttu-id="2a5c0-122">Определяет код задания, которое включает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a5c0-122">Specifies the ID of the job that this cmdlet enables.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a5c0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a5c0-123">CommonParameters</span></span>
<span data-ttu-id="2a5c0-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a5c0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a5c0-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a5c0-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a5c0-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2a5c0-126">INPUTS</span></span>

### <span data-ttu-id="2a5c0-127">System.String</span><span class="sxs-lookup"><span data-stu-id="2a5c0-127">System.String</span></span>

### <span data-ttu-id="2a5c0-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2a5c0-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="2a5c0-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2a5c0-129">OUTPUTS</span></span>

### <span data-ttu-id="2a5c0-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="2a5c0-130">System.Void</span></span>

## <span data-ttu-id="2a5c0-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2a5c0-131">NOTES</span></span>

## <span data-ttu-id="2a5c0-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a5c0-132">RELATED LINKS</span></span>

[<span data-ttu-id="2a5c0-133">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2a5c0-133">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="2a5c0-134">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2a5c0-134">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="2a5c0-135">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2a5c0-135">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="2a5c0-136">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2a5c0-136">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="2a5c0-137">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2a5c0-137">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="2a5c0-138">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="2a5c0-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
