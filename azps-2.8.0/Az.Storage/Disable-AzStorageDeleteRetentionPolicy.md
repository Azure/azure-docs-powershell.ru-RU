---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: fad4e01b06182d689e105f4b5e6c6a580e1b20b6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906942"
---
# <span data-ttu-id="f1e41-101">Disable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f1e41-101">Disable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="f1e41-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f1e41-102">SYNOPSIS</span></span>
<span data-ttu-id="f1e41-103">Отключите удаление политики хранения для службы больших двоичных объектов хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="f1e41-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="f1e41-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f1e41-104">SYNTAX</span></span>

```
Disable-AzStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1e41-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1e41-105">DESCRIPTION</span></span>
<span data-ttu-id="f1e41-106">Командлет **Disable-AzStorageDeleteRetentionPolicy** отключает удаление политики хранения для службы больших двоичных объектов хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="f1e41-106">The **Disable-AzStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="f1e41-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f1e41-107">EXAMPLES</span></span>

### <span data-ttu-id="f1e41-108">Пример 1: Отключение удаления политики хранения для службы больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="f1e41-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageDeleteRetentionPolicy
```

<span data-ttu-id="f1e41-109">Эта команда отключает удаление политики хранения для службы больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="f1e41-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="f1e41-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f1e41-110">PARAMETERS</span></span>

### <span data-ttu-id="f1e41-111">-Context</span><span class="sxs-lookup"><span data-stu-id="f1e41-111">-Context</span></span>
<span data-ttu-id="f1e41-112">Объект контекста хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="f1e41-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="f1e41-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1e41-113">-DefaultProfile</span></span>
<span data-ttu-id="f1e41-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f1e41-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1e41-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1e41-115">-PassThru</span></span>
<span data-ttu-id="f1e41-116">Показать DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="f1e41-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="f1e41-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1e41-117">-Confirm</span></span>
<span data-ttu-id="f1e41-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f1e41-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1e41-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1e41-119">-WhatIf</span></span>
<span data-ttu-id="f1e41-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f1e41-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1e41-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f1e41-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1e41-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1e41-122">CommonParameters</span></span>
<span data-ttu-id="f1e41-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f1e41-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1e41-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1e41-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1e41-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f1e41-125">INPUTS</span></span>

### <span data-ttu-id="f1e41-126">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f1e41-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f1e41-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1e41-127">OUTPUTS</span></span>

### <span data-ttu-id="f1e41-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f1e41-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="f1e41-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="f1e41-129">NOTES</span></span>

## <span data-ttu-id="f1e41-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f1e41-130">RELATED LINKS</span></span>
