---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
ms.openlocfilehash: e97e89c1ab7160f1eb06c9c94cd5620a48b0463e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246019"
---
# <span data-ttu-id="16af3-101">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="16af3-101">Enable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="16af3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="16af3-102">SYNOPSIS</span></span>
<span data-ttu-id="16af3-103">Включите статический веб-сайт для учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="16af3-103">Enable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="16af3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="16af3-104">SYNTAX</span></span>

```
Enable-AzStorageStaticWebsite [[-IndexDocument] <String>] [[-ErrorDocument404Path] <String>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="16af3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="16af3-105">DESCRIPTION</span></span>
<span data-ttu-id="16af3-106">Командлет **Enable-AzStorageStaticWebsite** включает статический веб-сайт для учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="16af3-106">The **Enable-AzStorageStaticWebsite** cmdlet enables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="16af3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="16af3-107">EXAMPLES</span></span>

### <span data-ttu-id="16af3-108">Пример 1: Включение статического веб-сайта для учетной записи хранения Azure</span><span class="sxs-lookup"><span data-stu-id="16af3-108">Example 1: Enable static website for the Azure Storage account</span></span>
```
C:\PS>Enable-AzStorageStaticWebsite -IndexDocument $indexdoc -ErrorDocument404Path $errordoc
```

<span data-ttu-id="16af3-109">Эта команда включает статический веб-сайт для учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="16af3-109">This command enables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="16af3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="16af3-110">PARAMETERS</span></span>

### <span data-ttu-id="16af3-111">-Context</span><span class="sxs-lookup"><span data-stu-id="16af3-111">-Context</span></span>
<span data-ttu-id="16af3-112">Объект контекста хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="16af3-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="16af3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16af3-113">-DefaultProfile</span></span>
<span data-ttu-id="16af3-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="16af3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16af3-115">-ErrorDocument404Path</span><span class="sxs-lookup"><span data-stu-id="16af3-115">-ErrorDocument404Path</span></span>
<span data-ttu-id="16af3-116">Путь к документу об ошибке, который должен отображаться при выдаче 404 (это означает, что веб-браузер запрашивает страницу, которая не существует).</span><span class="sxs-lookup"><span data-stu-id="16af3-116">The path to the error document that should be shown when a 404 is issued (meaning, when a browser requests a page that does not exist.)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16af3-117">-IndexDocument</span><span class="sxs-lookup"><span data-stu-id="16af3-117">-IndexDocument</span></span>
<span data-ttu-id="16af3-118">Имя индексируемого документа в каждом каталоге.</span><span class="sxs-lookup"><span data-stu-id="16af3-118">The name of the index document in each directory.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16af3-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16af3-119">-PassThru</span></span>
<span data-ttu-id="16af3-120">Отображать статические параметры веб-сайта в ServiceProperties.</span><span class="sxs-lookup"><span data-stu-id="16af3-120">Display Static Website setting in ServiceProperties.</span></span>

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

### <span data-ttu-id="16af3-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="16af3-121">-Confirm</span></span>
<span data-ttu-id="16af3-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="16af3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16af3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16af3-123">-WhatIf</span></span>
<span data-ttu-id="16af3-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="16af3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16af3-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="16af3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16af3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16af3-126">CommonParameters</span></span>
<span data-ttu-id="16af3-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="16af3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16af3-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16af3-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16af3-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="16af3-129">INPUTS</span></span>

### <span data-ttu-id="16af3-130">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="16af3-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="16af3-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="16af3-131">OUTPUTS</span></span>

### <span data-ttu-id="16af3-132">Microsoft. WindowsAzure. Commands. Storage. Model. ResourceModel. PSStaticWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="16af3-132">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="16af3-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="16af3-133">NOTES</span></span>

## <span data-ttu-id="16af3-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="16af3-134">RELATED LINKS</span></span>
