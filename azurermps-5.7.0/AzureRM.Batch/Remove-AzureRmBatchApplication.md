---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2CED21D6-4BEF-423B-A04A-5B812CEB975D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurermbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplication.md
ms.openlocfilehash: df7229668547e1c018067effe50e823354d64736
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569052"
---
# <span data-ttu-id="e1fc3-101">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="e1fc3-101">Remove-AzureRmBatchApplication</span></span>

## <span data-ttu-id="e1fc3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e1fc3-102">SYNOPSIS</span></span>
<span data-ttu-id="e1fc3-103">Удаляет приложение из пакетной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="e1fc3-103">Deletes an application from a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1fc3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e1fc3-104">SYNTAX</span></span>

```
Remove-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1fc3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1fc3-105">DESCRIPTION</span></span>
<span data-ttu-id="e1fc3-106">Командлет **Remove-AzureRmBatchApplication** удаляет приложение из пакетной учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="e1fc3-106">The **Remove-AzureRmBatchApplication** cmdlet deletes an application from an Azure Batch account.</span></span>

## <span data-ttu-id="e1fc3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e1fc3-107">EXAMPLES</span></span>

### <span data-ttu-id="e1fc3-108">Пример 1: Удаление приложения из пакетной учетной записи</span><span class="sxs-lookup"><span data-stu-id="e1fc3-108">Example 1: Delete an application from a Batch account</span></span>
```
PS C:\>Remove-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware"
```

<span data-ttu-id="e1fc3-109">Эта команда удаляет приложение беседа Litware из учетной записи ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="e1fc3-109">This command deletes the Litware application from the ContosoBatch account.</span></span>
<span data-ttu-id="e1fc3-110">Команда не выполняется, если приложение включает в себя пакеты.</span><span class="sxs-lookup"><span data-stu-id="e1fc3-110">The command fails if the application contains any packages.</span></span>

## <span data-ttu-id="e1fc3-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e1fc3-111">PARAMETERS</span></span>

### <span data-ttu-id="e1fc3-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="e1fc3-112">-AccountName</span></span>
<span data-ttu-id="e1fc3-113">Указывает имя пакетной учетной записи, из которой этот командлет удаляет приложение.</span><span class="sxs-lookup"><span data-stu-id="e1fc3-113">Specifies the name of the Batch account from which this cmdlet removes an application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1fc3-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="e1fc3-114">-ApplicationId</span></span>
<span data-ttu-id="e1fc3-115">Указывает идентификатор приложения.</span><span class="sxs-lookup"><span data-stu-id="e1fc3-115">Specifies the ID of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1fc3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1fc3-116">-DefaultProfile</span></span>
<span data-ttu-id="e1fc3-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e1fc3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1fc3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1fc3-118">-ResourceGroupName</span></span>
<span data-ttu-id="e1fc3-119">Указывает имя группы ресурсов, которая содержит пакетную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="e1fc3-119">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1fc3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1fc3-120">CommonParameters</span></span>
<span data-ttu-id="e1fc3-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e1fc3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1fc3-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1fc3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1fc3-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e1fc3-123">INPUTS</span></span>

### <span data-ttu-id="e1fc3-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="e1fc3-124">None</span></span>
<span data-ttu-id="e1fc3-125">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="e1fc3-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e1fc3-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1fc3-126">OUTPUTS</span></span>

## <span data-ttu-id="e1fc3-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="e1fc3-127">NOTES</span></span>

## <span data-ttu-id="e1fc3-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e1fc3-128">RELATED LINKS</span></span>

[<span data-ttu-id="e1fc3-129">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="e1fc3-129">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="e1fc3-130">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="e1fc3-130">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="e1fc3-131">New-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="e1fc3-131">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="e1fc3-132">New-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="e1fc3-132">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="e1fc3-133">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="e1fc3-133">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="e1fc3-134">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="e1fc3-134">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


