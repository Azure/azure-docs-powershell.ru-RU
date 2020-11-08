---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: c8a32cb86ace86cb0f2775db98f49f57408be6f4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246354"
---
# <span data-ttu-id="d12a6-101">Disable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d12a6-101">Disable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="d12a6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d12a6-102">SYNOPSIS</span></span>
<span data-ttu-id="d12a6-103">Отключите удаление политики хранения для службы больших двоичных объектов хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="d12a6-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="d12a6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d12a6-104">SYNTAX</span></span>

```
Disable-AzStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d12a6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d12a6-105">DESCRIPTION</span></span>
<span data-ttu-id="d12a6-106">Командлет **Disable-AzStorageDeleteRetentionPolicy** отключает удаление политики хранения для службы больших двоичных объектов хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="d12a6-106">The **Disable-AzStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="d12a6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d12a6-107">EXAMPLES</span></span>

### <span data-ttu-id="d12a6-108">Пример 1: Отключение удаления политики хранения для службы больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="d12a6-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageDeleteRetentionPolicy
```

<span data-ttu-id="d12a6-109">Эта команда отключает удаление политики хранения для службы больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="d12a6-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="d12a6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d12a6-110">PARAMETERS</span></span>

### <span data-ttu-id="d12a6-111">-Context</span><span class="sxs-lookup"><span data-stu-id="d12a6-111">-Context</span></span>
<span data-ttu-id="d12a6-112">Объект контекста хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="d12a6-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="d12a6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d12a6-113">-DefaultProfile</span></span>
<span data-ttu-id="d12a6-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d12a6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d12a6-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d12a6-115">-PassThru</span></span>
<span data-ttu-id="d12a6-116">Показать DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="d12a6-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="d12a6-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d12a6-117">-Confirm</span></span>
<span data-ttu-id="d12a6-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d12a6-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d12a6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d12a6-119">-WhatIf</span></span>
<span data-ttu-id="d12a6-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d12a6-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d12a6-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d12a6-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d12a6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d12a6-122">CommonParameters</span></span>
<span data-ttu-id="d12a6-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d12a6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d12a6-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d12a6-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d12a6-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d12a6-125">INPUTS</span></span>

### <span data-ttu-id="d12a6-126">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d12a6-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d12a6-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d12a6-127">OUTPUTS</span></span>

### <span data-ttu-id="d12a6-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d12a6-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="d12a6-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="d12a6-129">NOTES</span></span>

## <span data-ttu-id="d12a6-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d12a6-130">RELATED LINKS</span></span>
