---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 6A6D6C7D-EED7-4AD4-ACE6-BFA64404455E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchTask.md
ms.openlocfilehash: 7c3e976e85e6754702f8288f5bb257086837fc36
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509553"
---
# <span data-ttu-id="a7104-101">Set-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="a7104-101">Set-AzBatchTask</span></span>

## <span data-ttu-id="a7104-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7104-102">SYNOPSIS</span></span>
<span data-ttu-id="a7104-103">Обновляет свойства задачи.</span><span class="sxs-lookup"><span data-stu-id="a7104-103">Updates the properties of a task.</span></span>

## <span data-ttu-id="a7104-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a7104-104">SYNTAX</span></span>

```
Set-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7104-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7104-105">DESCRIPTION</span></span>
<span data-ttu-id="a7104-106">Для обновления свойств задачи в службе Azure Batch обновляется **cmdlet Set-AzBatchTask.**</span><span class="sxs-lookup"><span data-stu-id="a7104-106">The **Set-AzBatchTask** cmdlet updates the properties of a task in the Azure Batch service.</span></span>
<span data-ttu-id="a7104-107">Используйте Get-AzBatchTask для получения объекта **PSCloudTask.**</span><span class="sxs-lookup"><span data-stu-id="a7104-107">Use the Get-AzBatchTask cmdlet to get a **PSCloudTask** object.</span></span>
<span data-ttu-id="a7104-108">Измените свойства этого объекта, а затем с помощью текущего cmdlet зафиксировать изменения в пакетной службе.</span><span class="sxs-lookup"><span data-stu-id="a7104-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="a7104-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a7104-109">EXAMPLES</span></span>

### <span data-ttu-id="a7104-110">Пример 1. Обновление задачи</span><span class="sxs-lookup"><span data-stu-id="a7104-110">Example 1: Update a task</span></span>
```
PS C:\>$Task = Get-AzBatchTask -JobId "Job16" -Id "Task22" -BatchContext $Context
PS C:\> $Constraints = New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints -ArgumentList @([TimeSpan}::FromDays(5), [TimeSpan]::FromDays(2), 3)
PS C:\> $Task.Constraints = $Constraints
PS C:\> Set-AzBatchTask -Task $Task -BatchContext $Context
```

<span data-ttu-id="a7104-111">Первая команда получает задачу с помощью **Get-AzBatchTask,** а затем сохраняет ее в $Task переменной.</span><span class="sxs-lookup"><span data-stu-id="a7104-111">The first command gets a task by using **Get-AzBatchTask**, and then stores it in the $Task variable.</span></span>
<span data-ttu-id="a7104-112">Следующие две команды изменяют ограничения задачи в $Task.</span><span class="sxs-lookup"><span data-stu-id="a7104-112">The next two commands modify the constraints of the task in $Task.</span></span>
<span data-ttu-id="a7104-113">Конечная команда обновляет пакетную службу в соответствие с локальным объектом в $Task.</span><span class="sxs-lookup"><span data-stu-id="a7104-113">The final command updates the Batch service to match the local object in $Task.</span></span>

## <span data-ttu-id="a7104-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7104-114">PARAMETERS</span></span>

### <span data-ttu-id="a7104-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a7104-115">-BatchContext</span></span>
<span data-ttu-id="a7104-116">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="a7104-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a7104-117">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой batchy будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a7104-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a7104-118">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="a7104-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a7104-119">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a7104-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a7104-120">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="a7104-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a7104-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7104-121">-DefaultProfile</span></span>
<span data-ttu-id="a7104-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a7104-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7104-123">-Задача</span><span class="sxs-lookup"><span data-stu-id="a7104-123">-Task</span></span>
<span data-ttu-id="a7104-124">Определяет **PSCloudTask,** для которого этот cmdlet обновляет пакетную службу.</span><span class="sxs-lookup"><span data-stu-id="a7104-124">Specifies the **PSCloudTask** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7104-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7104-125">CommonParameters</span></span>
<span data-ttu-id="a7104-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7104-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7104-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7104-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7104-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a7104-128">INPUTS</span></span>

### <span data-ttu-id="a7104-129">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="a7104-129">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="a7104-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a7104-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a7104-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a7104-131">OUTPUTS</span></span>

### <span data-ttu-id="a7104-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="a7104-132">System.Void</span></span>

## <span data-ttu-id="a7104-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a7104-133">NOTES</span></span>

## <span data-ttu-id="a7104-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7104-134">RELATED LINKS</span></span>

[<span data-ttu-id="a7104-135">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="a7104-135">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="a7104-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="a7104-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="a7104-137">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="a7104-137">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="a7104-138">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="a7104-138">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="a7104-139">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="a7104-139">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="a7104-140">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="a7104-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
