---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: c8a32cb86ace86cb0f2775db98f49f57408be6f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100224980"
---
# <span data-ttu-id="39bbf-101">Disable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="39bbf-101">Disable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="39bbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39bbf-102">SYNOPSIS</span></span>
<span data-ttu-id="39bbf-103">Отключите политику хранения удаления для службы BLOB-документов хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="39bbf-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="39bbf-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="39bbf-104">SYNTAX</span></span>

```
Disable-AzStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39bbf-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="39bbf-105">DESCRIPTION</span></span>
<span data-ttu-id="39bbf-106">**Cmdlet Disable-AzStorageDeleteRetentionPolicy** отключает политику хранения удаления для службы BLOB-документов хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="39bbf-106">The **Disable-AzStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="39bbf-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="39bbf-107">EXAMPLES</span></span>

### <span data-ttu-id="39bbf-108">Пример 1. Отключение политики хранения удаления для службы BLOB-документов</span><span class="sxs-lookup"><span data-stu-id="39bbf-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageDeleteRetentionPolicy
```

<span data-ttu-id="39bbf-109">Эта команда отключает политику хранения удаления для службы BLOB-документов.</span><span class="sxs-lookup"><span data-stu-id="39bbf-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="39bbf-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39bbf-110">PARAMETERS</span></span>

### <span data-ttu-id="39bbf-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="39bbf-111">-Context</span></span>
<span data-ttu-id="39bbf-112">Контекстный объект хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="39bbf-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="39bbf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39bbf-113">-DefaultProfile</span></span>
<span data-ttu-id="39bbf-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="39bbf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39bbf-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39bbf-115">-PassThru</span></span>
<span data-ttu-id="39bbf-116">Отображение свойств DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="39bbf-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="39bbf-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39bbf-117">-Confirm</span></span>
<span data-ttu-id="39bbf-118">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39bbf-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39bbf-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39bbf-119">-WhatIf</span></span>
<span data-ttu-id="39bbf-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39bbf-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39bbf-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="39bbf-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39bbf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39bbf-122">CommonParameters</span></span>
<span data-ttu-id="39bbf-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39bbf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39bbf-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39bbf-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39bbf-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="39bbf-125">INPUTS</span></span>

### <span data-ttu-id="39bbf-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="39bbf-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="39bbf-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="39bbf-127">OUTPUTS</span></span>

### <span data-ttu-id="39bbf-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="39bbf-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="39bbf-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="39bbf-129">NOTES</span></span>

## <span data-ttu-id="39bbf-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="39bbf-130">RELATED LINKS</span></span>
