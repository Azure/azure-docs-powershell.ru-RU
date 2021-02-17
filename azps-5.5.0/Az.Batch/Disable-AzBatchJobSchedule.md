---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
ms.openlocfilehash: f874432bc26ae2a579a54e4068c719b236ad4c45
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239472"
---
# <span data-ttu-id="e25cb-101">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e25cb-101">Disable-AzBatchJobSchedule</span></span>

## <span data-ttu-id="e25cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e25cb-102">SYNOPSIS</span></span>
<span data-ttu-id="e25cb-103">Отключает расписание пакетных рабочих мест.</span><span class="sxs-lookup"><span data-stu-id="e25cb-103">Disables a Batch job schedule.</span></span>

## <span data-ttu-id="e25cb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e25cb-104">SYNTAX</span></span>

```
Disable-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e25cb-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e25cb-105">DESCRIPTION</span></span>
<span data-ttu-id="e25cb-106">**Cmdlet Disable-AzBatchJobSchedule** отключает расписание рабочих процессов Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="e25cb-106">The **Disable-AzBatchJobSchedule** cmdlet disables an Azure Batch job schedule.</span></span>
<span data-ttu-id="e25cb-107">Если отключить расписание, задания не будут создаваться согласно этому расписанию.</span><span class="sxs-lookup"><span data-stu-id="e25cb-107">If you disable a schedule, jobs are not created according to that schedule.</span></span>
<span data-ttu-id="e25cb-108">Отключив расписание, вы сможете включить его позднее.</span><span class="sxs-lookup"><span data-stu-id="e25cb-108">You can enable a disabled schedule later.</span></span>

## <span data-ttu-id="e25cb-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e25cb-109">EXAMPLES</span></span>

### <span data-ttu-id="e25cb-110">Пример 1. Отключение расписания работы</span><span class="sxs-lookup"><span data-stu-id="e25cb-110">Example 1: Disable a job schedule</span></span>
```
PS C:\>Disable-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="e25cb-111">Эта команда отключает расписание задания с расписанием задания ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="e25cb-111">This command disables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="e25cb-112">Чтобы назначить контекст переменной $Context, используйте $Context **AzBatchAccountKey.**</span><span class="sxs-lookup"><span data-stu-id="e25cb-112">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="e25cb-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e25cb-113">PARAMETERS</span></span>

### <span data-ttu-id="e25cb-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e25cb-114">-BatchContext</span></span>
<span data-ttu-id="e25cb-115">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="e25cb-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e25cb-116">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой batchy будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e25cb-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e25cb-117">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="e25cb-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e25cb-118">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e25cb-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e25cb-119">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="e25cb-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e25cb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e25cb-120">-DefaultProfile</span></span>
<span data-ttu-id="e25cb-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e25cb-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e25cb-122">-Id</span><span class="sxs-lookup"><span data-stu-id="e25cb-122">-Id</span></span>
<span data-ttu-id="e25cb-123">Определяет код расписания задания, который этот cmdlet отключает.</span><span class="sxs-lookup"><span data-stu-id="e25cb-123">Specifies the ID of the job schedule that this cmdlet disables.</span></span>

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

### <span data-ttu-id="e25cb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e25cb-124">CommonParameters</span></span>
<span data-ttu-id="e25cb-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e25cb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e25cb-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e25cb-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e25cb-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e25cb-127">INPUTS</span></span>

### <span data-ttu-id="e25cb-128">System.String</span><span class="sxs-lookup"><span data-stu-id="e25cb-128">System.String</span></span>

### <span data-ttu-id="e25cb-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e25cb-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e25cb-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e25cb-130">OUTPUTS</span></span>

### <span data-ttu-id="e25cb-131">System.Void</span><span class="sxs-lookup"><span data-stu-id="e25cb-131">System.Void</span></span>

## <span data-ttu-id="e25cb-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e25cb-132">NOTES</span></span>

## <span data-ttu-id="e25cb-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e25cb-133">RELATED LINKS</span></span>

[<span data-ttu-id="e25cb-134">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e25cb-134">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="e25cb-135">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="e25cb-135">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="e25cb-136">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e25cb-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="e25cb-137">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e25cb-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="e25cb-138">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e25cb-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="e25cb-139">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e25cb-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="e25cb-140">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="e25cb-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
