---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClientCertificate.md
ms.openlocfilehash: d1bd4dc4a3fd47d19d76568e9c60a51f09d739c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563992"
---
# <span data-ttu-id="ca7cf-101">Add-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ca7cf-101">Add-AzureRmServiceFabricClientCertificate</span></span>

## <span data-ttu-id="ca7cf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ca7cf-102">SYNOPSIS</span></span>
<span data-ttu-id="ca7cf-103">Добавьте в кластер общее имя или отпечаток для целей проверки подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="ca7cf-103">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca7cf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ca7cf-104">SYNTAX</span></span>

### <span data-ttu-id="ca7cf-105">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="ca7cf-105">SingleUpdateWithThumbprint</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca7cf-106">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="ca7cf-106">SingleUpdateWithCommonName</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca7cf-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="ca7cf-107">MultipleUpdatesWithCommonName</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca7cf-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="ca7cf-108">MultipleUpdatesWithThumbprint</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca7cf-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca7cf-109">DESCRIPTION</span></span>
<span data-ttu-id="ca7cf-110">С помощью **Add-AzureRmServiceFabricClientCertificate** добавьте в кластер общего имени и отпечаток поставщика или отпечаток сертификата, чтобы клиент мог использовать его для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="ca7cf-110">Use **Add-AzureRmServiceFabricClientCertificate** to add a common name and issuer thumbprint or certificate thumbprint to the cluster, so the client can use it for authentication.</span></span>

## <span data-ttu-id="ca7cf-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ca7cf-111">EXAMPLES</span></span>

### <span data-ttu-id="ca7cf-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ca7cf-112">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="ca7cf-113">Эта команда добавит сертификат с отпечатком "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" в кластер, чтобы клиент мог использовать этот сертификат в качестве администратора для связи с кластером.</span><span class="sxs-lookup"><span data-stu-id="ca7cf-113">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="ca7cf-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ca7cf-114">Example 2</span></span>
```
PS c:> Add-AzureRmServiceFabricClientCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="ca7cf-115">Эта команда добавит сертификат клиента только для чтения с общим именем "Contoso.com", а отпечаток поставщика — "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" в кластер.</span><span class="sxs-lookup"><span data-stu-id="ca7cf-115">This command will add a read only client certificate that's common name is 'Contoso.com' and issuer thumbprint is '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster.</span></span>

## <span data-ttu-id="ca7cf-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ca7cf-116">PARAMETERS</span></span>

### <span data-ttu-id="ca7cf-117">-Администратор</span><span class="sxs-lookup"><span data-stu-id="ca7cf-117">-Admin</span></span>
<span data-ttu-id="ca7cf-118">Тип проверки подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="ca7cf-118">Client authentication type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SingleUpdateWithThumbprint, SingleUpdateWithCommonName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca7cf-119">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="ca7cf-119">-AdminClientThumbprint</span></span>
<span data-ttu-id="ca7cf-120">Укажите отпечаток сертификата клиента, у которого есть разрешение администратора.</span><span class="sxs-lookup"><span data-stu-id="ca7cf-120">Specify client certificate thumbprint that only has admin permission.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca7cf-121">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="ca7cf-121">-ClientCertificateCommonName</span></span>
<span data-ttu-id="ca7cf-122">Укажите общее имя клиента, отпечаток поставщика и тип проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="ca7cf-122">Specify client common name, issuer thumbprint, and authentication type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]
Parameter Sets: MultipleUpdatesWithCommonName
Aliases: CertCommonName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca7cf-123">-CommonName</span><span class="sxs-lookup"><span data-stu-id="ca7cf-123">-CommonName</span></span>
<span data-ttu-id="ca7cf-124">Укажите общее имя сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="ca7cf-124">Specify client certificate common name.</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithCommonName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca7cf-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca7cf-125">-DefaultProfile</span></span>
<span data-ttu-id="ca7cf-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ca7cf-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca7cf-127">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="ca7cf-127">-IssuerThumbprint</span></span>
<span data-ttu-id="ca7cf-128">Укажите отпечаток поставщика сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="ca7cf-128">Specify client certificate issuer thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithCommonName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca7cf-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ca7cf-129">-Name</span></span>
<span data-ttu-id="ca7cf-130">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="ca7cf-130">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca7cf-131">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="ca7cf-131">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="ca7cf-132">Укажите отпечаток сертификата клиента с разрешением только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ca7cf-132">Specify client certificate thumbprint that has read only permission.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca7cf-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca7cf-133">-ResourceGroupName</span></span>
<span data-ttu-id="ca7cf-134">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ca7cf-134">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca7cf-135">-Отпечаток</span><span class="sxs-lookup"><span data-stu-id="ca7cf-135">-Thumbprint</span></span>
<span data-ttu-id="ca7cf-136">Укажите отпечаток сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="ca7cf-136">Specify client certificate thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithThumbprint
Aliases: ClientCertificateThumbprint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca7cf-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ca7cf-137">-Confirm</span></span>
<span data-ttu-id="ca7cf-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ca7cf-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca7cf-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca7cf-139">-WhatIf</span></span>
<span data-ttu-id="ca7cf-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ca7cf-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca7cf-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ca7cf-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca7cf-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca7cf-142">CommonParameters</span></span>
<span data-ttu-id="ca7cf-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ca7cf-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca7cf-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca7cf-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca7cf-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ca7cf-145">INPUTS</span></span>

### <span data-ttu-id="ca7cf-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ca7cf-146">System.Management.Automation.SwitchParameter</span></span>
<span data-ttu-id="ca7cf-147">Параметры: Администратор (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ca7cf-147">Parameters: Admin (ByValue)</span></span>

### <span data-ttu-id="ca7cf-148">System. String</span><span class="sxs-lookup"><span data-stu-id="ca7cf-148">System.String</span></span>
<span data-ttu-id="ca7cf-149">Параметры: CommonName (ByValue), IssuerThumbprint (ByValue), Thumbprint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ca7cf-149">Parameters: CommonName (ByValue), IssuerThumbprint (ByValue), Thumbprint (ByValue)</span></span>

### <span data-ttu-id="ca7cf-150">System. String []</span><span class="sxs-lookup"><span data-stu-id="ca7cf-150">System.String[]</span></span>
<span data-ttu-id="ca7cf-151">Параметры: AdminClientThumbprint (ByValue), ReadonlyClientThumbprint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ca7cf-151">Parameters: AdminClientThumbprint (ByValue), ReadonlyClientThumbprint (ByValue)</span></span>

### <span data-ttu-id="ca7cf-152">Microsoft. Azure. Commands. ServiceFabric. Models. PSClientCertificateCommonName []</span><span class="sxs-lookup"><span data-stu-id="ca7cf-152">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>
<span data-ttu-id="ca7cf-153">Параметры: ClientCertificateCommonName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ca7cf-153">Parameters: ClientCertificateCommonName (ByValue)</span></span>

## <span data-ttu-id="ca7cf-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca7cf-154">OUTPUTS</span></span>

### <span data-ttu-id="ca7cf-155">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="ca7cf-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="ca7cf-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="ca7cf-156">NOTES</span></span>

## <span data-ttu-id="ca7cf-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ca7cf-157">RELATED LINKS</span></span>

[<span data-ttu-id="ca7cf-158">Remove-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ca7cf-158">Remove-AzureRmServiceFabricClientCertificate</span></span>](./Remove-AzureRmServiceFabricClientCertificate.md)
