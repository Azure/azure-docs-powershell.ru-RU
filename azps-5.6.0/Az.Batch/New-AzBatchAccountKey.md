---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 486748AC-3932-4E0C-BBCC-2BC194E69DCC
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccountKey.md
ms.openlocfilehash: ee5ae846ed83065b797f1389827d7d53ae1988d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015523"
---
# <span data-ttu-id="58f3c-101">New-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="58f3c-101">New-AzBatchAccountKey</span></span>

## <span data-ttu-id="58f3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58f3c-102">SYNOPSIS</span></span>
<span data-ttu-id="58f3c-103">Повторное сгенерирует ключ учетной записи пакета.</span><span class="sxs-lookup"><span data-stu-id="58f3c-103">Regenerates a key of a Batch account.</span></span>

## <span data-ttu-id="58f3c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="58f3c-104">SYNTAX</span></span>

```
New-AzBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>] -KeyType <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58f3c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="58f3c-105">DESCRIPTION</span></span>
<span data-ttu-id="58f3c-106">Для повторного сгенерации основного или дополнительного ключа учетной записи Azure Batch будет повторно сгенерироваться **cmdlet New-AzBatchAccountKey.**</span><span class="sxs-lookup"><span data-stu-id="58f3c-106">The **New-AzBatchAccountKey** cmdlet regenerates the primary or secondary key of an Azure Batch account.</span></span>
<span data-ttu-id="58f3c-107">Этот cmdlet возвращает объект **BatchAccountContext** с текущими свойствами **PrimaryAccountKey** и **SecondaryAccountKey.**</span><span class="sxs-lookup"><span data-stu-id="58f3c-107">The cmdlet returns a **BatchAccountContext** object that has its current **PrimaryAccountKey** and **SecondaryAccountKey** properties.</span></span>

## <span data-ttu-id="58f3c-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="58f3c-108">EXAMPLES</span></span>

### <span data-ttu-id="58f3c-109">Пример 1. Повторное сгенерировать первичный ключ учетной записи в пакетной учетной записи</span><span class="sxs-lookup"><span data-stu-id="58f3c-109">Example 1: Regenerate the primary account key on a Batch account</span></span>
```
PS C:\>New-AzBatchAccountKey -AccountName "pfuller" -KeyType "Primary"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="58f3c-110">Эта команда повторно сгенерирует первичный ключ учетной записи в пакетной учетной записи с именем pfuller.</span><span class="sxs-lookup"><span data-stu-id="58f3c-110">This command regenerates the primary account key on the Batch account named pfuller.</span></span>

## <span data-ttu-id="58f3c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58f3c-111">PARAMETERS</span></span>

### <span data-ttu-id="58f3c-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="58f3c-112">-AccountName</span></span>
<span data-ttu-id="58f3c-113">Имя учетной записи пакета, для которой этот cmdlet повторно сгенерирует ключ.</span><span class="sxs-lookup"><span data-stu-id="58f3c-113">Specifies the name of the Batch account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="58f3c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58f3c-114">-DefaultProfile</span></span>
<span data-ttu-id="58f3c-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="58f3c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58f3c-116">-KeyType</span><span class="sxs-lookup"><span data-stu-id="58f3c-116">-KeyType</span></span>
<span data-ttu-id="58f3c-117">Определяет тип ключа, который повторно сгенерирует этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58f3c-117">Specifies the type of key that this cmdlet regenerates.</span></span>
<span data-ttu-id="58f3c-118">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="58f3c-118">Valid values are:</span></span>
- <span data-ttu-id="58f3c-119">Primary</span><span class="sxs-lookup"><span data-stu-id="58f3c-119">Primary</span></span>
- <span data-ttu-id="58f3c-120">Secondary</span><span class="sxs-lookup"><span data-stu-id="58f3c-120">Secondary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58f3c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58f3c-121">-ResourceGroupName</span></span>
<span data-ttu-id="58f3c-122">Определяет группу ресурсов учетной записи, для которой этот cmdlet повторно сгенерирует ключ.</span><span class="sxs-lookup"><span data-stu-id="58f3c-122">Specifies the resource group of the account for which this cmdlet regenerates a key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58f3c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58f3c-123">CommonParameters</span></span>
<span data-ttu-id="58f3c-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58f3c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58f3c-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58f3c-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58f3c-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="58f3c-126">INPUTS</span></span>

### <span data-ttu-id="58f3c-127">System.String</span><span class="sxs-lookup"><span data-stu-id="58f3c-127">System.String</span></span>

## <span data-ttu-id="58f3c-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="58f3c-128">OUTPUTS</span></span>

### <span data-ttu-id="58f3c-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="58f3c-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="58f3c-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="58f3c-130">NOTES</span></span>

## <span data-ttu-id="58f3c-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="58f3c-131">RELATED LINKS</span></span>

[<span data-ttu-id="58f3c-132">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="58f3c-132">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="58f3c-133">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="58f3c-133">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
