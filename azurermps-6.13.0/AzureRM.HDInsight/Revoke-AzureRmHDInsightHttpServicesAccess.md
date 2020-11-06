---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 670EAFC0-3F8D-4F3D-8B62-448F04378F8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/revoke-azurermhdinsighthttpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightHttpServicesAccess.md
ms.openlocfilehash: 93024e0719687c10ec07daa7269d742db012abe9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568550"
---
# <span data-ttu-id="0ad69-101">Revoke-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0ad69-101">Revoke-AzureRmHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="0ad69-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0ad69-102">SYNOPSIS</span></span>
<span data-ttu-id="0ad69-103">Отключает доступ к кластеру через HTTP.</span><span class="sxs-lookup"><span data-stu-id="0ad69-103">Disables HTTP access to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ad69-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0ad69-104">SYNTAX</span></span>

```
Revoke-AzureRmHDInsightHttpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ad69-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ad69-105">DESCRIPTION</span></span>
<span data-ttu-id="0ad69-106">Командлет **REVOKE-AzureRmHDInsightHttpServicesAccess** отключает доступ HTTP к кластеру HDInsight Azure для ODBC, Ambari, Oozie и webHCatalog веб-службам.</span><span class="sxs-lookup"><span data-stu-id="0ad69-106">The **Revoke-AzureRmHDInsightHttpServicesAccess** cmdlet disables HTTP access to an Azure HDInsight cluster for ODBC, Ambari, Oozie and webHCatalog web services.</span></span>

## <span data-ttu-id="0ad69-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0ad69-107">EXAMPLES</span></span>

### <span data-ttu-id="0ad69-108">Пример 1: отключение доступа HTTP к кластеру</span><span class="sxs-lookup"><span data-stu-id="0ad69-108">Example 1: Disable HTTP access to a cluster</span></span>
```
PS C:\>Revoke-AzureRmHDInsightHttpServicesAccess `
       -ClusterName "your-hadoop_001"
```

<span data-ttu-id="0ad69-109">Эта команда отменяет доступ по протоколу HTTP к кластеру с именем hadoop_001.</span><span class="sxs-lookup"><span data-stu-id="0ad69-109">This command revokes HTTP access to the cluster named your-hadoop_001.</span></span>

## <span data-ttu-id="0ad69-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0ad69-110">PARAMETERS</span></span>

### <span data-ttu-id="0ad69-111">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="0ad69-111">-ClusterName</span></span>
<span data-ttu-id="0ad69-112">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="0ad69-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="0ad69-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ad69-113">-DefaultProfile</span></span>
<span data-ttu-id="0ad69-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0ad69-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0ad69-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ad69-115">-ResourceGroupName</span></span>
<span data-ttu-id="0ad69-116">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0ad69-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="0ad69-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ad69-117">CommonParameters</span></span>
<span data-ttu-id="0ad69-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0ad69-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ad69-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ad69-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ad69-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0ad69-120">INPUTS</span></span>

### <span data-ttu-id="0ad69-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="0ad69-121">None</span></span>

## <span data-ttu-id="0ad69-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ad69-122">OUTPUTS</span></span>

### <span data-ttu-id="0ad69-123">Microsoft. Azure. Management. HDInsight. Models. HttpConnectivitySettings</span><span class="sxs-lookup"><span data-stu-id="0ad69-123">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="0ad69-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="0ad69-124">NOTES</span></span>

## <span data-ttu-id="0ad69-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0ad69-125">RELATED LINKS</span></span>

[<span data-ttu-id="0ad69-126">Grant-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0ad69-126">Grant-AzureRmHDInsightHttpServicesAccess</span></span>](./Grant-AzureRmHDInsightHttpServicesAccess.md)


