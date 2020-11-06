---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 486748AC-3932-4E0C-BBCC-2BC194E69DCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurermbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccountKey.md
ms.openlocfilehash: 48de3ae521f77c531433ffca67dadc9e2c46a980
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567816"
---
# <span data-ttu-id="9f19a-101">New-AzureRmBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="9f19a-101">New-AzureRmBatchAccountKey</span></span>

## <span data-ttu-id="9f19a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9f19a-102">SYNOPSIS</span></span>
<span data-ttu-id="9f19a-103">Повторное создание ключа учетной записи пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="9f19a-103">Regenerates a key of a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f19a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9f19a-104">SYNTAX</span></span>

```
New-AzureRmBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>] -KeyType <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f19a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f19a-105">DESCRIPTION</span></span>
<span data-ttu-id="9f19a-106">Командлет **New-AzureRmBatchAccountKey** заново создает первичный или вторичный ключ для пакетной учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="9f19a-106">The **New-AzureRmBatchAccountKey** cmdlet regenerates the primary or secondary key of an Azure Batch account.</span></span>
<span data-ttu-id="9f19a-107">Командлет возвращает объект **BatchAccountContext** с текущими свойствами **PrimaryAccountKey** и **SecondaryAccountKey** .</span><span class="sxs-lookup"><span data-stu-id="9f19a-107">The cmdlet returns a **BatchAccountContext** object that has its current **PrimaryAccountKey** and **SecondaryAccountKey** properties.</span></span>

## <span data-ttu-id="9f19a-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9f19a-108">EXAMPLES</span></span>

### <span data-ttu-id="9f19a-109">Пример 1: повторное создание первичного ключа учетной записи для пакетной учетной записи</span><span class="sxs-lookup"><span data-stu-id="9f19a-109">Example 1: Regenerate the primary account key on a Batch account</span></span>
```
PS C:\>New-AzureRmBatchAccountKey -AccountName "pfuller" -KeyType "Primary"
AccountName                  : pfuller

Location                     : westus

ResourceGroupName            : CmdletExampleRG

CoreQuota                    : 20

PoolQuota                    : 20

ActiveJobAndJobScheduleQuota : 20

Tags                         : 
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="9f19a-110">Эта команда повторно создает первичный ключ учетной записи для пакетной учетной записи с именем pfuller.</span><span class="sxs-lookup"><span data-stu-id="9f19a-110">This command regenerates the primary account key on the Batch account named pfuller.</span></span>

## <span data-ttu-id="9f19a-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9f19a-111">PARAMETERS</span></span>

### <span data-ttu-id="9f19a-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="9f19a-112">-AccountName</span></span>
<span data-ttu-id="9f19a-113">Указывает имя пакетной учетной записи, для которой этот командлет заново создает ключ.</span><span class="sxs-lookup"><span data-stu-id="9f19a-113">Specifies the name of the Batch account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="9f19a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f19a-114">-DefaultProfile</span></span>
<span data-ttu-id="9f19a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9f19a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f19a-116">-KeyType</span><span class="sxs-lookup"><span data-stu-id="9f19a-116">-KeyType</span></span>
<span data-ttu-id="9f19a-117">Указывает тип ключа, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="9f19a-117">Specifies the type of key that this cmdlet regenerates.</span></span>
<span data-ttu-id="9f19a-118">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="9f19a-118">Valid values are:</span></span> 
- <span data-ttu-id="9f19a-119">Главная</span><span class="sxs-lookup"><span data-stu-id="9f19a-119">Primary</span></span>
- <span data-ttu-id="9f19a-120">Запас</span><span class="sxs-lookup"><span data-stu-id="9f19a-120">Secondary</span></span>

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

### <span data-ttu-id="9f19a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f19a-121">-ResourceGroupName</span></span>
<span data-ttu-id="9f19a-122">Указывает группу ресурсов для учетной записи, для которой этот командлет заново создает ключ.</span><span class="sxs-lookup"><span data-stu-id="9f19a-122">Specifies the resource group of the account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="9f19a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f19a-123">CommonParameters</span></span>
<span data-ttu-id="9f19a-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9f19a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f19a-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f19a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f19a-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9f19a-126">INPUTS</span></span>

### <span data-ttu-id="9f19a-127">System. String</span><span class="sxs-lookup"><span data-stu-id="9f19a-127">System.String</span></span>

## <span data-ttu-id="9f19a-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f19a-128">OUTPUTS</span></span>

### <span data-ttu-id="9f19a-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9f19a-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="9f19a-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="9f19a-130">NOTES</span></span>

## <span data-ttu-id="9f19a-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f19a-131">RELATED LINKS</span></span>

[<span data-ttu-id="9f19a-132">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="9f19a-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="9f19a-133">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="9f19a-133">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


