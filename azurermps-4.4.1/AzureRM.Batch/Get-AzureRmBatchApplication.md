---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: CF8B8E94-3C6C-4D68-B55B-956393890946
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplication.md
ms.openlocfilehash: b8169b2f05b4272c92989768e672b30aee105f19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568088"
---
# <span data-ttu-id="dff1c-101">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="dff1c-101">Get-AzureRmBatchApplication</span></span>

## <span data-ttu-id="dff1c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dff1c-102">SYNOPSIS</span></span>
<span data-ttu-id="dff1c-103">Получает сведения о указанном приложении.</span><span class="sxs-lookup"><span data-stu-id="dff1c-103">Gets information about the specified application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dff1c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dff1c-104">SYNTAX</span></span>

```
Get-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [[-ApplicationId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dff1c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dff1c-105">DESCRIPTION</span></span>
<span data-ttu-id="dff1c-106">Командлет **Get-AzureRmBatchApplication** получает сведения о приложении в пакетной учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="dff1c-106">The **Get-AzureRmBatchApplication** cmdlet gets information about an application in an Azure Batch account.</span></span>

## <span data-ttu-id="dff1c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dff1c-107">EXAMPLES</span></span>

### <span data-ttu-id="dff1c-108">Пример 1: отображение приложений в пакетной учетной записи</span><span class="sxs-lookup"><span data-stu-id="dff1c-108">Example 1: Display the applications in a Batch account</span></span>
```
PS C:\>Get-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup"
ApplicationId AllowUpdates DisplayName

------------- ------------ ----------------------------

litware       False        Litware Advanced Reticulator
```

<span data-ttu-id="dff1c-109">Эта команда отображает все приложения в учетной записи ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="dff1c-109">This command displays all applications in the ContosoBatch account.</span></span>

## <span data-ttu-id="dff1c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dff1c-110">PARAMETERS</span></span>

### <span data-ttu-id="dff1c-111">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="dff1c-111">-AccountName</span></span>
<span data-ttu-id="dff1c-112">Указывает имя пакетной учетной записи, содержащей приложение.</span><span class="sxs-lookup"><span data-stu-id="dff1c-112">Specifies the name of the Batch account that contains the application.</span></span>

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

### <span data-ttu-id="dff1c-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="dff1c-113">-ApplicationId</span></span>
<span data-ttu-id="dff1c-114">Указывает идентификатор приложения.</span><span class="sxs-lookup"><span data-stu-id="dff1c-114">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="dff1c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dff1c-115">-ResourceGroupName</span></span>
<span data-ttu-id="dff1c-116">Указывает имя группы ресурсов, которая содержит пакетную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="dff1c-116">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="dff1c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dff1c-117">-DefaultProfile</span></span>
<span data-ttu-id="dff1c-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dff1c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dff1c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dff1c-119">CommonParameters</span></span>
<span data-ttu-id="dff1c-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dff1c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dff1c-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dff1c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dff1c-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dff1c-122">INPUTS</span></span>

## <span data-ttu-id="dff1c-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dff1c-123">OUTPUTS</span></span>

### <span data-ttu-id="dff1c-124">Microsoft.Azure.Commands.BatCH. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="dff1c-124">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="dff1c-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="dff1c-125">NOTES</span></span>

## <span data-ttu-id="dff1c-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dff1c-126">RELATED LINKS</span></span>

[<span data-ttu-id="dff1c-127">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="dff1c-127">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="dff1c-128">New-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="dff1c-128">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="dff1c-129">New-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="dff1c-129">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="dff1c-130">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="dff1c-130">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="dff1c-131">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="dff1c-131">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="dff1c-132">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="dff1c-132">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


