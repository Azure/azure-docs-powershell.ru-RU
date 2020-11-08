---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
ms.openlocfilehash: a7814734f33e0a68fefacf4e465c1834cce17708
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065723"
---
# <span data-ttu-id="f7955-101">Disable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f7955-101">Disable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="f7955-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f7955-102">SYNOPSIS</span></span>
<span data-ttu-id="f7955-103">Отключение статического веб-сайта для учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="f7955-103">Disable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="f7955-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f7955-104">SYNTAX</span></span>

```
Disable-AzStorageStaticWebsite [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7955-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7955-105">DESCRIPTION</span></span>
<span data-ttu-id="f7955-106">Командлет **Disable-AzStorageStaticWebsite** отключает статический веб-сайт для учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="f7955-106">The **Disable-AzStorageStaticWebsite** cmdlet disables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="f7955-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f7955-107">EXAMPLES</span></span>

### <span data-ttu-id="f7955-108">Пример 1: отключение статического веб-сайта для учетной записи хранения Azure</span><span class="sxs-lookup"><span data-stu-id="f7955-108">Example 1: Disable static website for a Azure Storage account</span></span>
```
C:\PS>Disable-AzStorageStaticWebsite
```

<span data-ttu-id="f7955-109">Эта команда отключает статический веб-сайт для учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="f7955-109">This command disables static website for a Azure Storage account.</span></span>

## <span data-ttu-id="f7955-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f7955-110">PARAMETERS</span></span>

### <span data-ttu-id="f7955-111">-Context</span><span class="sxs-lookup"><span data-stu-id="f7955-111">-Context</span></span>
<span data-ttu-id="f7955-112">Объект контекста хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="f7955-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="f7955-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7955-113">-DefaultProfile</span></span>
<span data-ttu-id="f7955-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f7955-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7955-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f7955-115">-PassThru</span></span>
<span data-ttu-id="f7955-116">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="f7955-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f7955-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7955-117">-Confirm</span></span>
<span data-ttu-id="f7955-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f7955-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7955-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7955-119">-WhatIf</span></span>
<span data-ttu-id="f7955-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f7955-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7955-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f7955-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7955-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7955-122">CommonParameters</span></span>
<span data-ttu-id="f7955-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f7955-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7955-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7955-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7955-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f7955-125">INPUTS</span></span>

### <span data-ttu-id="f7955-126">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f7955-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f7955-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7955-127">OUTPUTS</span></span>

### <span data-ttu-id="f7955-128">Microsoft. WindowsAzure. Commands. Storage. Model. ResourceModel. PSStaticWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="f7955-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="f7955-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="f7955-129">NOTES</span></span>

## <span data-ttu-id="f7955-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7955-130">RELATED LINKS</span></span>
