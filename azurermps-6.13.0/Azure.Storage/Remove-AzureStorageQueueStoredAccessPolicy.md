---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 1f5c97824a9296954f2c7bad742b5f8176359563
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567342"
---
# <span data-ttu-id="82f09-101">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="82f09-101">Remove-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="82f09-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="82f09-102">SYNOPSIS</span></span>
<span data-ttu-id="82f09-103">Удаляет политику сохраненного доступа из очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="82f09-103">Removes a stored access policy from an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82f09-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="82f09-104">SYNTAX</span></span>

```
Remove-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="82f09-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="82f09-105">DESCRIPTION</span></span>
<span data-ttu-id="82f09-106">Командлет **Remove-AzureStorageQueueStoredAccessPolicy** удаляет политику сохраненного доступа из очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="82f09-106">The **Remove-AzureStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="82f09-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="82f09-107">EXAMPLES</span></span>

### <span data-ttu-id="82f09-108">Пример 1: Удаление политики сохраненного доступа из очереди хранилища</span><span class="sxs-lookup"><span data-stu-id="82f09-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="82f09-109">Эта команда удаляет политику доступа с именем Policy04 из очереди хранения с именем MyQueue.</span><span class="sxs-lookup"><span data-stu-id="82f09-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="82f09-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="82f09-110">PARAMETERS</span></span>

### <span data-ttu-id="82f09-111">-Context</span><span class="sxs-lookup"><span data-stu-id="82f09-111">-Context</span></span>
<span data-ttu-id="82f09-112">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="82f09-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="82f09-113">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="82f09-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82f09-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82f09-114">-DefaultProfile</span></span>
<span data-ttu-id="82f09-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="82f09-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82f09-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="82f09-116">-PassThru</span></span>
<span data-ttu-id="82f09-117">Указывает на то, что этот командлет возвращает **логическое значение** , отражающее успешное выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="82f09-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="82f09-118">По умолчанию этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="82f09-118">By default, this cmdlet does not return a value.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f09-119">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="82f09-119">-Policy</span></span>
<span data-ttu-id="82f09-120">Указывает имя политики хранения, которая удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="82f09-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="82f09-121">-Очередь</span><span class="sxs-lookup"><span data-stu-id="82f09-121">-Queue</span></span>
<span data-ttu-id="82f09-122">Указывает имя очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="82f09-122">Specifies the Azure storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82f09-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82f09-123">-Confirm</span></span>
<span data-ttu-id="82f09-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="82f09-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f09-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82f09-125">-WhatIf</span></span>
<span data-ttu-id="82f09-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="82f09-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82f09-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="82f09-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f09-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82f09-128">CommonParameters</span></span>
<span data-ttu-id="82f09-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="82f09-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82f09-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82f09-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82f09-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="82f09-131">INPUTS</span></span>

### <span data-ttu-id="82f09-132">System. String</span><span class="sxs-lookup"><span data-stu-id="82f09-132">System.String</span></span>

### <span data-ttu-id="82f09-133">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="82f09-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="82f09-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="82f09-134">OUTPUTS</span></span>

### <span data-ttu-id="82f09-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="82f09-135">System.Boolean</span></span>

## <span data-ttu-id="82f09-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="82f09-136">NOTES</span></span>

## <span data-ttu-id="82f09-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="82f09-137">RELATED LINKS</span></span>

[<span data-ttu-id="82f09-138">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="82f09-138">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="82f09-139">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="82f09-139">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="82f09-140">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="82f09-140">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="82f09-141">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="82f09-141">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)
