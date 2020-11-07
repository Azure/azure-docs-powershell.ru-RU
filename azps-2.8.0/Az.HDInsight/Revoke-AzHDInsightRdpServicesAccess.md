---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8C6D9533-68FD-4AFF-91FB-8307A8C8EAEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/revoke-azhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Revoke-AzHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Revoke-AzHDInsightRdpServicesAccess.md
ms.openlocfilehash: 7f5fcb8dcfbb325b8bc0381b3c943e550fe27e62
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720802"
---
# <span data-ttu-id="73fa6-101">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="73fa6-101">Revoke-AzHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="73fa6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="73fa6-102">SYNOPSIS</span></span>
<span data-ttu-id="73fa6-103">Запрещает RDP-доступ к кластеру Windows.</span><span class="sxs-lookup"><span data-stu-id="73fa6-103">Disables RDP access to a Windows cluster.</span></span>

## <span data-ttu-id="73fa6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="73fa6-104">SYNTAX</span></span>

```
Revoke-AzHDInsightRdpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73fa6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="73fa6-105">DESCRIPTION</span></span>
<span data-ttu-id="73fa6-106">Командлет **REVOKE-AzHDInsightRdpServicesAccess** отключает доступ к протоколу удаленного рабочего стола (RDP) к кластеру Azure HDInsight на базе Windows.</span><span class="sxs-lookup"><span data-stu-id="73fa6-106">The **Revoke-AzHDInsightRdpServicesAccess** cmdlet disables Remote Desktop Protocol (RDP) access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="73fa6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="73fa6-107">EXAMPLES</span></span>

### <span data-ttu-id="73fa6-108">Пример 1: отключение доступа к указанному кластеру через RDP</span><span class="sxs-lookup"><span data-stu-id="73fa6-108">Example 1: Disable RDP access to a specified cluster</span></span>
```
PS C:\>Revoke-AzHDInsightRdpServicesAccess -ClusterName "your-hadoop-001"
```

<span data-ttu-id="73fa6-109">Эта команда запрещает доступ по протоколу RDP к кластеру с именем-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="73fa6-109">This command revokes RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="73fa6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="73fa6-110">PARAMETERS</span></span>

### <span data-ttu-id="73fa6-111">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="73fa6-111">-ClusterName</span></span>
<span data-ttu-id="73fa6-112">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="73fa6-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="73fa6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73fa6-113">-DefaultProfile</span></span>
<span data-ttu-id="73fa6-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="73fa6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73fa6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73fa6-115">-ResourceGroupName</span></span>
<span data-ttu-id="73fa6-116">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="73fa6-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="73fa6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73fa6-117">CommonParameters</span></span>
<span data-ttu-id="73fa6-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="73fa6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73fa6-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73fa6-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73fa6-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="73fa6-120">INPUTS</span></span>

### <span data-ttu-id="73fa6-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="73fa6-121">None</span></span>

## <span data-ttu-id="73fa6-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="73fa6-122">OUTPUTS</span></span>

### <span data-ttu-id="73fa6-123">System. void</span><span class="sxs-lookup"><span data-stu-id="73fa6-123">System.Void</span></span>

## <span data-ttu-id="73fa6-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="73fa6-124">NOTES</span></span>

## <span data-ttu-id="73fa6-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="73fa6-125">RELATED LINKS</span></span>

[<span data-ttu-id="73fa6-126">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="73fa6-126">Grant-AzHDInsightRdpServicesAccess</span></span>](./Grant-AzHDInsightRdpServicesAccess.md)


