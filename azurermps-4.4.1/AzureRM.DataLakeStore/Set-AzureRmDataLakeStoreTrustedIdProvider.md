---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: BDEF8BAA-0C64-465D-9ED4-6FEFC1E850CC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 12e84ee5456acc0c56eed0f35b0bf3c23813b31f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559827"
---
# <span data-ttu-id="8c508-101">Set-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="8c508-101">Set-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="8c508-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8c508-102">SYNOPSIS</span></span>
<span data-ttu-id="8c508-103">Изменяет указанного доверенного поставщика удостоверений в указанном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8c508-103">Modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c508-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8c508-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8c508-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c508-105">DESCRIPTION</span></span>
<span data-ttu-id="8c508-106">Командлет **Set-AzureRmDataLakeStoreTrustedIdProvider** изменяет указанный доверенный поставщик удостоверений в указанном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8c508-106">The **Set-AzureRmDataLakeStoreTrustedIdProvider** cmdlet modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="8c508-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8c508-107">EXAMPLES</span></span>

### <span data-ttu-id="8c508-108">Пример 1: обновление доверенной конечной точки поставщика удостоверений</span><span class="sxs-lookup"><span data-stu-id="8c508-108">Example 1: Update a Trusted Identity Provider Endpoint</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="8c508-109">Это обновление поставщика endpoing для правила межсетевого экрана "MyProvider" в учетной записи "ContosoADL" на " https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 "</span><span class="sxs-lookup"><span data-stu-id="8c508-109">This updates the provider endpoing for firewall rule "MyProvider" in account "ContosoADL" to "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="8c508-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8c508-110">PARAMETERS</span></span>

### <span data-ttu-id="8c508-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="8c508-111">-Account</span></span>
<span data-ttu-id="8c508-112">Учетная запись Data Lake Store для добавления доверенного поставщика удостоверений</span><span class="sxs-lookup"><span data-stu-id="8c508-112">The Data Lake Store account to add the trusted identity provider to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c508-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8c508-113">-Name</span></span>
<span data-ttu-id="8c508-114">Имя надежного поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="8c508-114">The name of the trusted identity provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c508-115">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="8c508-115">-ProviderEndpoint</span></span>
<span data-ttu-id="8c508-116">Правильная конечная точка доверенного поставщика в формате: https://sts.windows.net/\<provider identity\></span><span class="sxs-lookup"><span data-stu-id="8c508-116">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\></span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c508-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c508-117">-ResourceGroupName</span></span>
<span data-ttu-id="8c508-118">Указывает имя группы ресурсов, которая содержит учетную запись, для которой нужно обновить доверенный поставщик удостоверений.</span><span class="sxs-lookup"><span data-stu-id="8c508-118">Specifies the name of the resource group that contains the account to update the trusted identity provider for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c508-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c508-119">-Confirm</span></span>
<span data-ttu-id="8c508-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8c508-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c508-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c508-121">-WhatIf</span></span>
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

### <span data-ttu-id="8c508-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c508-122">-DefaultProfile</span></span>
<span data-ttu-id="8c508-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8c508-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c508-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c508-124">CommonParameters</span></span>
<span data-ttu-id="8c508-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8c508-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c508-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c508-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c508-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8c508-127">INPUTS</span></span>

## <span data-ttu-id="8c508-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c508-128">OUTPUTS</span></span>

### <span data-ttu-id="8c508-129">DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="8c508-129">DataLakeStoreTrustedIdProvider</span></span>
<span data-ttu-id="8c508-130">Обновленный доверенный поставщик удостоверений.</span><span class="sxs-lookup"><span data-stu-id="8c508-130">The updated trusted identity provider.</span></span>

## <span data-ttu-id="8c508-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="8c508-131">NOTES</span></span>

## <span data-ttu-id="8c508-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8c508-132">RELATED LINKS</span></span>

