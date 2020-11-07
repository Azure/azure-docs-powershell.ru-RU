---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2CED21D6-4BEF-423B-A04A-5B812CEB975D
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
ms.openlocfilehash: 2a449235ac2b3fa98357e91e15602a0c7bd9eedb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727691"
---
# <span data-ttu-id="f140d-101">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="f140d-101">Remove-AzBatchApplication</span></span>

## <span data-ttu-id="f140d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f140d-102">SYNOPSIS</span></span>
<span data-ttu-id="f140d-103">Удаляет приложение из пакетной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f140d-103">Deletes an application from a Batch account.</span></span>

## <span data-ttu-id="f140d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f140d-104">SYNTAX</span></span>

```
Remove-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f140d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f140d-105">DESCRIPTION</span></span>
<span data-ttu-id="f140d-106">Командлет **Remove-AzBatchApplication** удаляет приложение из пакетной учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="f140d-106">The **Remove-AzBatchApplication** cmdlet deletes an application from an Azure Batch account.</span></span>

## <span data-ttu-id="f140d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f140d-107">EXAMPLES</span></span>

### <span data-ttu-id="f140d-108">Пример 1: Удаление приложения из пакетной учетной записи</span><span class="sxs-lookup"><span data-stu-id="f140d-108">Example 1: Delete an application from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware"
```

<span data-ttu-id="f140d-109">Эта команда удаляет приложение беседа Litware из учетной записи ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="f140d-109">This command deletes the Litware application from the ContosoBatch account.</span></span>
<span data-ttu-id="f140d-110">Команда не выполняется, если приложение включает в себя пакеты.</span><span class="sxs-lookup"><span data-stu-id="f140d-110">The command fails if the application contains any packages.</span></span>

## <span data-ttu-id="f140d-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f140d-111">PARAMETERS</span></span>

### <span data-ttu-id="f140d-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="f140d-112">-AccountName</span></span>
<span data-ttu-id="f140d-113">Указывает имя пакетной учетной записи, из которой этот командлет удаляет приложение.</span><span class="sxs-lookup"><span data-stu-id="f140d-113">Specifies the name of the Batch account from which this cmdlet removes an application.</span></span>

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

### <span data-ttu-id="f140d-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="f140d-114">-ApplicationId</span></span>
<span data-ttu-id="f140d-115">Указывает идентификатор приложения.</span><span class="sxs-lookup"><span data-stu-id="f140d-115">Specifies the ID of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f140d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f140d-116">-DefaultProfile</span></span>
<span data-ttu-id="f140d-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f140d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f140d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f140d-118">-ResourceGroupName</span></span>
<span data-ttu-id="f140d-119">Указывает имя группы ресурсов, которая содержит пакетную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="f140d-119">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="f140d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f140d-120">CommonParameters</span></span>
<span data-ttu-id="f140d-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f140d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f140d-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f140d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f140d-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f140d-123">INPUTS</span></span>

### <span data-ttu-id="f140d-124">System. String</span><span class="sxs-lookup"><span data-stu-id="f140d-124">System.String</span></span>

## <span data-ttu-id="f140d-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f140d-125">OUTPUTS</span></span>

### <span data-ttu-id="f140d-126">System. void</span><span class="sxs-lookup"><span data-stu-id="f140d-126">System.Void</span></span>

## <span data-ttu-id="f140d-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="f140d-127">NOTES</span></span>

## <span data-ttu-id="f140d-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f140d-128">RELATED LINKS</span></span>

[<span data-ttu-id="f140d-129">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="f140d-129">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="f140d-130">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="f140d-130">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="f140d-131">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="f140d-131">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="f140d-132">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="f140d-132">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="f140d-133">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="f140d-133">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="f140d-134">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="f140d-134">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


