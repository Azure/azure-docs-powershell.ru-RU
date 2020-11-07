---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: CF8B8E94-3C6C-4D68-B55B-956393890946
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplication.md
ms.openlocfilehash: fa08214e141d035e7c449e591f6a4820f758b48c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731473"
---
# <span data-ttu-id="5b47f-101">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="5b47f-101">Get-AzBatchApplication</span></span>

## <span data-ttu-id="5b47f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5b47f-102">SYNOPSIS</span></span>
<span data-ttu-id="5b47f-103">Получает сведения о указанном приложении.</span><span class="sxs-lookup"><span data-stu-id="5b47f-103">Gets information about the specified application.</span></span>

## <span data-ttu-id="5b47f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5b47f-104">SYNTAX</span></span>

```
Get-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [[-ApplicationId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b47f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b47f-105">DESCRIPTION</span></span>
<span data-ttu-id="5b47f-106">Командлет **Get-AzBatchApplication** получает сведения о приложении в пакетной учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="5b47f-106">The **Get-AzBatchApplication** cmdlet gets information about an application in an Azure Batch account.</span></span>

## <span data-ttu-id="5b47f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5b47f-107">EXAMPLES</span></span>

### <span data-ttu-id="5b47f-108">Пример 1: отображение приложений в пакетной учетной записи</span><span class="sxs-lookup"><span data-stu-id="5b47f-108">Example 1: Display the applications in a Batch account</span></span>
```
PS C:\>Get-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup"
ApplicationId AllowUpdates DisplayName

------------- ------------ ----------------------------

litware       False        Litware Advanced Reticulator
```

<span data-ttu-id="5b47f-109">Эта команда отображает все приложения в учетной записи ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="5b47f-109">This command displays all applications in the ContosoBatch account.</span></span>

## <span data-ttu-id="5b47f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5b47f-110">PARAMETERS</span></span>

### <span data-ttu-id="5b47f-111">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="5b47f-111">-AccountName</span></span>
<span data-ttu-id="5b47f-112">Указывает имя пакетной учетной записи, содержащей приложение.</span><span class="sxs-lookup"><span data-stu-id="5b47f-112">Specifies the name of the Batch account that contains the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b47f-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="5b47f-113">-ApplicationId</span></span>
<span data-ttu-id="5b47f-114">Указывает идентификатор приложения.</span><span class="sxs-lookup"><span data-stu-id="5b47f-114">Specifies the ID of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b47f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b47f-115">-DefaultProfile</span></span>
<span data-ttu-id="5b47f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5b47f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b47f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b47f-117">-ResourceGroupName</span></span>
<span data-ttu-id="5b47f-118">Указывает имя группы ресурсов, которая содержит пакетную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="5b47f-118">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b47f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b47f-119">CommonParameters</span></span>
<span data-ttu-id="5b47f-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5b47f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b47f-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b47f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b47f-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5b47f-122">INPUTS</span></span>

### <span data-ttu-id="5b47f-123">System. String</span><span class="sxs-lookup"><span data-stu-id="5b47f-123">System.String</span></span>

## <span data-ttu-id="5b47f-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b47f-124">OUTPUTS</span></span>

### <span data-ttu-id="5b47f-125">Microsoft.Azure.Commands.BatCH. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="5b47f-125">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="5b47f-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="5b47f-126">NOTES</span></span>

## <span data-ttu-id="5b47f-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5b47f-127">RELATED LINKS</span></span>

[<span data-ttu-id="5b47f-128">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="5b47f-128">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="5b47f-129">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="5b47f-129">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="5b47f-130">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="5b47f-130">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="5b47f-131">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="5b47f-131">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="5b47f-132">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="5b47f-132">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="5b47f-133">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="5b47f-133">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


