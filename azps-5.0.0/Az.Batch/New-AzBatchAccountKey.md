---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 486748AC-3932-4E0C-BBCC-2BC194E69DCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccountKey.md
ms.openlocfilehash: 121e4b4b2ffe25d9e5ae53cb03e60cb7a1da91b2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247657"
---
# <span data-ttu-id="8ce5f-101">New-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="8ce5f-101">New-AzBatchAccountKey</span></span>

## <span data-ttu-id="8ce5f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8ce5f-102">SYNOPSIS</span></span>
<span data-ttu-id="8ce5f-103">Повторное создание ключа учетной записи пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="8ce5f-103">Regenerates a key of a Batch account.</span></span>

## <span data-ttu-id="8ce5f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8ce5f-104">SYNTAX</span></span>

```
New-AzBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>] -KeyType <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ce5f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ce5f-105">DESCRIPTION</span></span>
<span data-ttu-id="8ce5f-106">Командлет **New-AzBatchAccountKey** заново создает первичный или вторичный ключ для пакетной учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="8ce5f-106">The **New-AzBatchAccountKey** cmdlet regenerates the primary or secondary key of an Azure Batch account.</span></span>
<span data-ttu-id="8ce5f-107">Командлет возвращает объект **BatchAccountContext** с текущими свойствами **PrimaryAccountKey** и **SecondaryAccountKey** .</span><span class="sxs-lookup"><span data-stu-id="8ce5f-107">The cmdlet returns a **BatchAccountContext** object that has its current **PrimaryAccountKey** and **SecondaryAccountKey** properties.</span></span>

## <span data-ttu-id="8ce5f-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8ce5f-108">EXAMPLES</span></span>

### <span data-ttu-id="8ce5f-109">Пример 1: повторное создание первичного ключа учетной записи для пакетной учетной записи</span><span class="sxs-lookup"><span data-stu-id="8ce5f-109">Example 1: Regenerate the primary account key on a Batch account</span></span>
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

<span data-ttu-id="8ce5f-110">Эта команда повторно создает первичный ключ учетной записи для пакетной учетной записи с именем pfuller.</span><span class="sxs-lookup"><span data-stu-id="8ce5f-110">This command regenerates the primary account key on the Batch account named pfuller.</span></span>

## <span data-ttu-id="8ce5f-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8ce5f-111">PARAMETERS</span></span>

### <span data-ttu-id="8ce5f-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="8ce5f-112">-AccountName</span></span>
<span data-ttu-id="8ce5f-113">Указывает имя пакетной учетной записи, для которой этот командлет заново создает ключ.</span><span class="sxs-lookup"><span data-stu-id="8ce5f-113">Specifies the name of the Batch account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="8ce5f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ce5f-114">-DefaultProfile</span></span>
<span data-ttu-id="8ce5f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8ce5f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ce5f-116">-KeyType</span><span class="sxs-lookup"><span data-stu-id="8ce5f-116">-KeyType</span></span>
<span data-ttu-id="8ce5f-117">Указывает тип ключа, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="8ce5f-117">Specifies the type of key that this cmdlet regenerates.</span></span>
<span data-ttu-id="8ce5f-118">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="8ce5f-118">Valid values are:</span></span>
- <span data-ttu-id="8ce5f-119">Главная</span><span class="sxs-lookup"><span data-stu-id="8ce5f-119">Primary</span></span>
- <span data-ttu-id="8ce5f-120">Запас</span><span class="sxs-lookup"><span data-stu-id="8ce5f-120">Secondary</span></span>

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

### <span data-ttu-id="8ce5f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ce5f-121">-ResourceGroupName</span></span>
<span data-ttu-id="8ce5f-122">Указывает группу ресурсов для учетной записи, для которой этот командлет заново создает ключ.</span><span class="sxs-lookup"><span data-stu-id="8ce5f-122">Specifies the resource group of the account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="8ce5f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ce5f-123">CommonParameters</span></span>
<span data-ttu-id="8ce5f-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8ce5f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ce5f-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ce5f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ce5f-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8ce5f-126">INPUTS</span></span>

### <span data-ttu-id="8ce5f-127">System. String</span><span class="sxs-lookup"><span data-stu-id="8ce5f-127">System.String</span></span>

## <span data-ttu-id="8ce5f-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ce5f-128">OUTPUTS</span></span>

### <span data-ttu-id="8ce5f-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8ce5f-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="8ce5f-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="8ce5f-130">NOTES</span></span>

## <span data-ttu-id="8ce5f-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8ce5f-131">RELATED LINKS</span></span>

[<span data-ttu-id="8ce5f-132">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="8ce5f-132">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="8ce5f-133">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="8ce5f-133">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
