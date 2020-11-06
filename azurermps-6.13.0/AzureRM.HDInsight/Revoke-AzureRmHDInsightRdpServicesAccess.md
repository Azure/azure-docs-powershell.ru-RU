---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 8C6D9533-68FD-4AFF-91FB-8307A8C8EAEB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/revoke-azurermhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightRdpServicesAccess.md
ms.openlocfilehash: 8c3fd2340c1e15d5229a5fdfe9331b1d31c8c02a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568549"
---
# <span data-ttu-id="b346f-101">Revoke-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="b346f-101">Revoke-AzureRmHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="b346f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b346f-102">SYNOPSIS</span></span>
<span data-ttu-id="b346f-103">Запрещает RDP-доступ к кластеру Windows.</span><span class="sxs-lookup"><span data-stu-id="b346f-103">Disables RDP access to a Windows cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b346f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b346f-104">SYNTAX</span></span>

```
Revoke-AzureRmHDInsightRdpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b346f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b346f-105">DESCRIPTION</span></span>
<span data-ttu-id="b346f-106">Командлет **REVOKE-AzureRmHDInsightRdpServicesAccess** отключает доступ к протоколу удаленного рабочего стола (RDP) к кластеру Azure HDInsight на базе Windows.</span><span class="sxs-lookup"><span data-stu-id="b346f-106">The **Revoke-AzureRmHDInsightRdpServicesAccess** cmdlet disables Remote Desktop Protocol (RDP) access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="b346f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b346f-107">EXAMPLES</span></span>

### <span data-ttu-id="b346f-108">Пример 1: отключение доступа к указанному кластеру через RDP</span><span class="sxs-lookup"><span data-stu-id="b346f-108">Example 1: Disable RDP access to a specified cluster</span></span>
```
PS C:\>Revoke-AzureRmHDInsightRdpServicesAccess -ClusterName "your-hadoop-001"
```

<span data-ttu-id="b346f-109">Эта команда запрещает доступ по протоколу RDP к кластеру с именем-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="b346f-109">This command revokes RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="b346f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b346f-110">PARAMETERS</span></span>

### <span data-ttu-id="b346f-111">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="b346f-111">-ClusterName</span></span>
<span data-ttu-id="b346f-112">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="b346f-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="b346f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b346f-113">-DefaultProfile</span></span>
<span data-ttu-id="b346f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b346f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b346f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b346f-115">-ResourceGroupName</span></span>
<span data-ttu-id="b346f-116">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b346f-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b346f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b346f-117">CommonParameters</span></span>
<span data-ttu-id="b346f-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b346f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b346f-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b346f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b346f-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b346f-120">INPUTS</span></span>

### <span data-ttu-id="b346f-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="b346f-121">None</span></span>

## <span data-ttu-id="b346f-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b346f-122">OUTPUTS</span></span>

### <span data-ttu-id="b346f-123">System. void</span><span class="sxs-lookup"><span data-stu-id="b346f-123">System.Void</span></span>

## <span data-ttu-id="b346f-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="b346f-124">NOTES</span></span>

## <span data-ttu-id="b346f-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b346f-125">RELATED LINKS</span></span>

[<span data-ttu-id="b346f-126">Grant-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="b346f-126">Grant-AzureRmHDInsightRdpServicesAccess</span></span>](./Grant-AzureRmHDInsightRdpServicesAccess.md)


