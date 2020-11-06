---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/stop-azurermaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Stop-AzureRmAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Stop-AzureRmAksDashboard.md
ms.openlocfilehash: 4ec1c8c2788469ffd377127bc58f657c817434a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567029"
---
# <span data-ttu-id="373a1-101">Stop-AzureRmAksDashboard</span><span class="sxs-lookup"><span data-stu-id="373a1-101">Stop-AzureRmAksDashboard</span></span>

## <span data-ttu-id="373a1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="373a1-102">SYNOPSIS</span></span>
<span data-ttu-id="373a1-103">Остановите туннель SSH Kubectl, созданный в Start-AzureRmKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="373a1-103">Stop the Kubectl SSH tunnel created in Start-AzureRmKubernetesDashboard.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="373a1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="373a1-104">SYNTAX</span></span>

```
Stop-AzureRmAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="373a1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="373a1-105">DESCRIPTION</span></span>
<span data-ttu-id="373a1-106">Остановите туннель SSH Kubectl, созданный в Start-AzureRmKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="373a1-106">Stop the Kubectl SSH tunnel created in Start-AzureRmKubernetesDashboard.</span></span>

## <span data-ttu-id="373a1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="373a1-107">EXAMPLES</span></span>

### <span data-ttu-id="373a1-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="373a1-108">Example 1</span></span>
```
PS C:\> Stop-AzureRmKubernetesDashboard
```

<span data-ttu-id="373a1-109">Останавливает существующую настройку туннеля SSH, выполняя Start-AzureRmKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="373a1-109">Stops the existing SSH tunnel setup by executing Start-AzureRmKubernetesDashboard.</span></span>

## <span data-ttu-id="373a1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="373a1-110">PARAMETERS</span></span>

### <span data-ttu-id="373a1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="373a1-111">-DefaultProfile</span></span>
<span data-ttu-id="373a1-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="373a1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="373a1-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="373a1-113">-PassThru</span></span>
<span data-ttu-id="373a1-114">Возвращает значение истина, если закрытие туннеля SSH закрыто.</span><span class="sxs-lookup"><span data-stu-id="373a1-114">Returns true if SSH tunnel is closed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="373a1-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="373a1-115">CommonParameters</span></span>
<span data-ttu-id="373a1-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="373a1-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="373a1-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="373a1-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="373a1-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="373a1-118">INPUTS</span></span>

### <span data-ttu-id="373a1-119">Ничего</span><span class="sxs-lookup"><span data-stu-id="373a1-119">None</span></span>

## <span data-ttu-id="373a1-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="373a1-120">OUTPUTS</span></span>

### <span data-ttu-id="373a1-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="373a1-121">System.Boolean</span></span>

## <span data-ttu-id="373a1-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="373a1-122">NOTES</span></span>

## <span data-ttu-id="373a1-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="373a1-123">RELATED LINKS</span></span>
