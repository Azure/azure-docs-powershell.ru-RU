---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJobSchedule.md
ms.openlocfilehash: 03decd5b1d32defb25692220c63ffe768445697e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239429"
---
# <span data-ttu-id="9abc7-101">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9abc7-101">Enable-AzBatchJobSchedule</span></span>

## <span data-ttu-id="9abc7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9abc7-102">SYNOPSIS</span></span>
<span data-ttu-id="9abc7-103">Включает расписание пакетных рабочих мест.</span><span class="sxs-lookup"><span data-stu-id="9abc7-103">Enables a Batch job schedule.</span></span>

## <span data-ttu-id="9abc7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9abc7-104">SYNTAX</span></span>

```
Enable-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9abc7-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9abc7-105">DESCRIPTION</span></span>
<span data-ttu-id="9abc7-106">С **помощью cmdlet Enable-AzBatchJobSchedule** можно включить расписание рабочих мест Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="9abc7-106">The **Enable-AzBatchJobSchedule** cmdlet enables an Azure Batch job schedule.</span></span>
<span data-ttu-id="9abc7-107">После того как вы в включить расписание заданий, задания можно создавать по этому расписанию.</span><span class="sxs-lookup"><span data-stu-id="9abc7-107">After you enable a job schedule, jobs can be created according to that schedule.</span></span>

## <span data-ttu-id="9abc7-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9abc7-108">EXAMPLES</span></span>

### <span data-ttu-id="9abc7-109">Пример 1. Включить расписание работы</span><span class="sxs-lookup"><span data-stu-id="9abc7-109">Example 1: Enable a job schedule</span></span>
```
PS C:\>Enable-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="9abc7-110">Эта команда включает расписание задания с расписанием задания ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="9abc7-110">This command enables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="9abc7-111">Чтобы назначить контекст переменной $Context, используйте $Context **AzBatchAccountKey.**</span><span class="sxs-lookup"><span data-stu-id="9abc7-111">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="9abc7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9abc7-112">PARAMETERS</span></span>

### <span data-ttu-id="9abc7-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="9abc7-113">-BatchContext</span></span>
<span data-ttu-id="9abc7-114">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="9abc7-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9abc7-115">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой batchy будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9abc7-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="9abc7-116">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="9abc7-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="9abc7-117">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9abc7-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="9abc7-118">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="9abc7-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="9abc7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9abc7-119">-DefaultProfile</span></span>
<span data-ttu-id="9abc7-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9abc7-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9abc7-121">-Id</span><span class="sxs-lookup"><span data-stu-id="9abc7-121">-Id</span></span>
<span data-ttu-id="9abc7-122">Определяет код расписания задания, который включает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9abc7-122">Specifies the ID of the job schedule that this cmdlet enables.</span></span>

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

### <span data-ttu-id="9abc7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9abc7-123">CommonParameters</span></span>
<span data-ttu-id="9abc7-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9abc7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9abc7-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9abc7-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9abc7-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9abc7-126">INPUTS</span></span>

### <span data-ttu-id="9abc7-127">System.String</span><span class="sxs-lookup"><span data-stu-id="9abc7-127">System.String</span></span>

### <span data-ttu-id="9abc7-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9abc7-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="9abc7-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9abc7-129">OUTPUTS</span></span>

### <span data-ttu-id="9abc7-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="9abc7-130">System.Void</span></span>

## <span data-ttu-id="9abc7-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9abc7-131">NOTES</span></span>

## <span data-ttu-id="9abc7-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9abc7-132">RELATED LINKS</span></span>

[<span data-ttu-id="9abc7-133">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9abc7-133">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="9abc7-134">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="9abc7-134">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="9abc7-135">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9abc7-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="9abc7-136">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9abc7-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="9abc7-137">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9abc7-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="9abc7-138">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9abc7-138">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="9abc7-139">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="9abc7-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
