---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/enable-azurestoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Enable-AzureStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Enable-AzureStorageDeleteRetentionPolicy.md
ms.openlocfilehash: 4778e0230cd50b3567cb0ded2ca629cd81db33fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558679"
---
# <span data-ttu-id="d779e-101">Enable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d779e-101">Enable-AzureStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="d779e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d779e-102">SYNOPSIS</span></span>
<span data-ttu-id="d779e-103">Включите удаление политики хранения для службы больших двоичных объектов хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="d779e-103">Enable delete retention policy  for the Azure Storage Blob service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d779e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d779e-104">SYNTAX</span></span>

```
Enable-AzureStorageDeleteRetentionPolicy [-RetentionDays] <Int32> [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d779e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d779e-105">DESCRIPTION</span></span>
<span data-ttu-id="d779e-106">Командлет **Enable-AzureStorageDeleteRetentionPolicy** включает удаление политики хранения для службы больших двоичных объектов хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="d779e-106">The **Enable-AzureStorageDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="d779e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d779e-107">EXAMPLES</span></span>

### <span data-ttu-id="d779e-108">Пример 1: Включение удаления политики хранения для службы больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="d779e-108">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzureStorageDeleteRetentionPolicy -RetentionDays 3
```

<span data-ttu-id="d779e-109">Эта команда включает удаление политики хранения для службы больших двоичных объектов и присвойте удаленным дням хранения BLOB-данных значение 3.</span><span class="sxs-lookup"><span data-stu-id="d779e-109">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 3.</span></span>

## <span data-ttu-id="d779e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d779e-110">PARAMETERS</span></span>

### <span data-ttu-id="d779e-111">-Context</span><span class="sxs-lookup"><span data-stu-id="d779e-111">-Context</span></span>
<span data-ttu-id="d779e-112">Объект контекста хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="d779e-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="d779e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d779e-113">-DefaultProfile</span></span>
<span data-ttu-id="d779e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d779e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d779e-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d779e-115">-PassThru</span></span>
<span data-ttu-id="d779e-116">Показать DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="d779e-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="d779e-117">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="d779e-117">-RetentionDays</span></span>
<span data-ttu-id="d779e-118">Задает количество дней хранения для DeleteRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="d779e-118">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Days

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d779e-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d779e-119">-Confirm</span></span>
<span data-ttu-id="d779e-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d779e-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d779e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d779e-121">-WhatIf</span></span>
<span data-ttu-id="d779e-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d779e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d779e-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d779e-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d779e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d779e-124">CommonParameters</span></span>
<span data-ttu-id="d779e-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d779e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d779e-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d779e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d779e-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d779e-127">INPUTS</span></span>

### <span data-ttu-id="d779e-128">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d779e-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d779e-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d779e-129">OUTPUTS</span></span>

### <span data-ttu-id="d779e-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d779e-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="d779e-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="d779e-131">NOTES</span></span>

## <span data-ttu-id="d779e-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d779e-132">RELATED LINKS</span></span>
