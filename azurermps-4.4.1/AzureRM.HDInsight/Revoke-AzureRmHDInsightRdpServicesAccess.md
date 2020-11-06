---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 8C6D9533-68FD-4AFF-91FB-8307A8C8EAEB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightRdpServicesAccess.md
ms.openlocfilehash: f05cae3484067f227fde8f30cd7806307832b185
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559800"
---
# <span data-ttu-id="37970-101">Revoke-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="37970-101">Revoke-AzureRmHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="37970-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="37970-102">SYNOPSIS</span></span>
<span data-ttu-id="37970-103">Запрещает RDP-доступ к кластеру Windows.</span><span class="sxs-lookup"><span data-stu-id="37970-103">Disables RDP access to a Windows cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37970-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="37970-104">SYNTAX</span></span>

```
Revoke-AzureRmHDInsightRdpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37970-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="37970-105">DESCRIPTION</span></span>
<span data-ttu-id="37970-106">Командлет **REVOKE-AzureRmHDInsightRdpServicesAccess** отключает доступ к протоколу удаленного рабочего стола (RDP) к кластеру Azure HDInsight на базе Windows.</span><span class="sxs-lookup"><span data-stu-id="37970-106">The **Revoke-AzureRmHDInsightRdpServicesAccess** cmdlet disables Remote Desktop Protocol (RDP) access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="37970-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="37970-107">EXAMPLES</span></span>

### <span data-ttu-id="37970-108">Пример 1: отключение доступа к указанному кластеру через RDP</span><span class="sxs-lookup"><span data-stu-id="37970-108">Example 1: Disable RDP access to a specified cluster</span></span>
```
PS C:\>Revoke-AzureRmHDInsightRdpServicesAccess -ClusterName "your-hadoop-001"
```

<span data-ttu-id="37970-109">Эта команда запрещает доступ по протоколу RDP к кластеру с именем-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="37970-109">This command revokes RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="37970-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="37970-110">PARAMETERS</span></span>

### <span data-ttu-id="37970-111">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="37970-111">-ClusterName</span></span>
<span data-ttu-id="37970-112">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="37970-112">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37970-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37970-113">-ResourceGroupName</span></span>
<span data-ttu-id="37970-114">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="37970-114">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37970-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37970-115">-DefaultProfile</span></span>
<span data-ttu-id="37970-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="37970-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37970-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37970-117">CommonParameters</span></span>
<span data-ttu-id="37970-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="37970-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37970-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37970-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37970-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="37970-120">INPUTS</span></span>

## <span data-ttu-id="37970-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="37970-121">OUTPUTS</span></span>

### <span data-ttu-id="37970-122">System. void</span><span class="sxs-lookup"><span data-stu-id="37970-122">System.Void</span></span>

## <span data-ttu-id="37970-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="37970-123">NOTES</span></span>

## <span data-ttu-id="37970-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="37970-124">RELATED LINKS</span></span>

[<span data-ttu-id="37970-125">Grant-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="37970-125">Grant-AzureRmHDInsightRdpServicesAccess</span></span>](./Grant-AzureRmHDInsightRdpServicesAccess.md)


